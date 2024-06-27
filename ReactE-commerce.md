In these notes i will write every detail which i experience during creating E-commerce application.


<h2 style='color:red; font-size: 30px; font-weight: 700;'>Create React App</h2>

```
npm create vite@latest
```
<h2 style='color:red; font-size: 30px; font-weight: 700;'>Want shortHand?</h2>

```
npm install react-dom react-router-dom @reduxjs/toolkit react-redux @fortawesome/fontawesome-svg-core @fortawesome/free-solid-svg-icons @mui/material @mui/icons-material
```

<h2 style='color:red; font-size: 30px; font-weight: 700;'>Add tailwind if need</h2>

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

> configureyour template path

```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

```

> Add the Tailwind directives

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

<h2 style='color:red; font-size: 30px; font-weight: 700;'>Add React Router Dom</h2>

```
npm install react-dom react-router-dom
```

> Provide the React Router to React

```
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App.jsx";
import "./index.css";
import { Provider } from "react-redux";
import { store } from "./feathers/store.js";
import { RouterProvider, createBrowserRouter } from "react-router-dom";
import Home from "./components/Home.jsx";
import Cart from "./components/Cart.jsx";
import ProductView from "./components/ProductView.jsx";

const router = createBrowserRouter([
  {
    path: "/",
    element: <App />,
    children: [
      {
        path: "",
        element: <Home />,
      },
      {
        path: "cart",
        element: <Cart />,
      },
      {
        path: "productView",
        element: <ProductView />,
      },
    ],
  },
]);

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
      <RouterProvider router={router} />
  </React.StrictMode>
);
```

<h2 style='color:red; font-size: 30px; font-weight: 700;'>Add Redux toolkit and setUp</h2>

```
npm install @reduxjs/toolkit react-redux
```

> Create Redux Store

```
import { configureStore } from '@reduxjs/toolkit'

export const store = configureStore({
  reducer: {},
})
```

> Provide the Redux store to React

```
import React from 'react'
import ReactDOM from 'react-dom'
import './index.css'
import App from './App'
import { store } from './app/store'
import { Provider } from 'react-redux'

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('root')
)
```

> Creating Slice which will call the api and error handling

```
import { createSlice, createAsyncThunk } from '@reduxjs/toolkit';

export const fetchData = createAsyncThunk(
  'yourFeature/fetchData',
  async () => {
    const response = await fetch('https://dummyjson.com/products');
    // 'https://fakestoreapi.com/products?limit=50'
    const data = await response.json();
    // console.log(data.products);
    return data.products;
  }
);

const apiSlice = createSlice({
  name: 'api',
  initialState: {
    data: [],
    status: 'idle',
    error: null,
  },
  reducers: {},
  extraReducers: (builder) => {
    builder
      .addCase(fetchData.pending, (state) => {
        state.status = 'loading';
      })
      .addCase(fetchData.fulfilled, (state, action) => {
        state.status = 'succeeded';
        state.data = action.payload;
      })
      .addCase(fetchData.rejected, (state, action) => {
        state.status = 'failed';
        state.error = action.error.message;
      });
  },
});

export default apiSlice.reducer;

```

> Give access this slice to store

```
api: apiReducer,
```

> Use Fetched data and error handling functionalities

```
import React, { useEffect } from "react";
import { useSelector, useDispatch } from "react-redux";
import { fetchData } from "../feathers/apiSlice";
import Product from "./Product";

function Home() {
  const dispatch = useDispatch();
  const data = useSelector((state) => state.api.data);
  const status = useSelector((state) => state.api.status);
  const error = useSelector((state) => state.api.error);

  useEffect(() => {
    if (status === "idle") {
      dispatch(fetchData());
    }
  }, [status, dispatch]);

  if (status === "loading") {
    return <div>Loading...</div>;
  } else if (status === "failed") {
    return <div>Error: {error}</div>;
  }
  // console.log(data);
  return (
    <>
      <div className="items">
        {data.map(item => {
          return <Product data={item} />
        })}
      </div>
    </>
  );
}

export default Home;
```

<h2 style='color:red; font-size: 30px; font-weight: 700;'>Some feathers which mostly every E commerce application have:</h2>

```
fetchData from api and error handling
addToCart
RemoveFromCart
IncreaseQuantity
DecreaseQuantity
SelectProduct and show that product data for better view
clearSelectedProduct, which selected while selectingProduct
```

## codes for the above functionalities

```
import { createSlice } from "@reduxjs/toolkit";

const initialState = {
  items: [],
};

const cartSlice = createSlice({
  name: "cart",
  initialState,
  reducers: {
    addToCart: (state, action) => {
      const item = action.payload;
      const existingItem = state.items.find((i) => i.id === item.id);

      if (existingItem) {
        existingItem.quantity += 1;
      } else {
        state.items.push({ ...item, quantity: 1 });
      }
    },
    removeFromCart: (state, action) => {
      const itemId = action.payload;
      state.items = state.items.filter((item) => item.id !== itemId);
    },
    increaseQuantity: (state, action) => {
      const itemId = action.payload;
      const item = state.items.find((i) => i.id === itemId);
      if (item) {
        item.quantity += 1;
      }
    },
    decreaseQuantity: (state, action) => {
      const itemId = action.payload;
      const item = state.items.find((i) => i.id === itemId);
      if (item && item.quantity > 1) {
        item.quantity -= 1;
      }
    },
  },
});

export const { addToCart, removeFromCart, increaseQuantity, decreaseQuantity } =
  cartSlice.actions;
export default cartSlice.reducer;

```

> Select and clear Product

```
import { createSlice } from '@reduxjs/toolkit';

const initialState = {
  selectedProduct: null,
};

const productSlice = createSlice({
  name: 'product',
  initialState,
  reducers: {
    selectProduct(state, action) {
      state.selectedProduct = action.payload;
    },
    clearSelectedProduct(state) {
      state.selectedProduct = null;
    }
  },
});

export const { selectProduct, clearSelectedProduct } = productSlice.actions;
export default productSlice.reducer;
```

## Then use NavLink and Link to navigate setup

We can add style attribute the `NavLink` but we can'not style `Link`.

## How to add FontAwsome icon in app
```
npm install @fortawesome/fontawesome-svg-core @fortawesome/free-solid-svg-icons
```
> import `Fontawesome` and icon name
```
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';
import { faCartShopping } from '@fortawesome/free-solid-svg-icons';
```
> Then code code form website and paste where need

## How to add Mui components in React
```
npm install @mui/material @mui/icons-material
```
> After installation import component and icon by name
```
import { IconButton } from '@mui/material';
import { Mail } from '@mui/icons-material';
```
> Copy code for mui and paste in code and use accordingly
```
if not understand copy code form mui and go to chatGPT and paste ask for guidince how to use it in react
```

## Additional Information

1. We can give parametrized function in `onClick` using callback function. Without callback parametrized funciton atomatically called.
2. Also we have to manage TotalPrice, Discount, Quantity in cart Component
3. Use icon of mui for adding cart feather

## Next Task

1. I need to create a beautiful alert when user add item to cart
2. I need to show data according to categories
3. I need to add search functionalitie
4. I need to store it on browser storage
5. I need to add animations for more creativity
