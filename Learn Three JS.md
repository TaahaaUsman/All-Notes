In this lecture I will learn what matters for `Three js`.

<h1 style='font-size: 40px; color: red; text-align: center;'>Full notes of Three JS</h1>

<h2 style='color: aquamarine;' align='center'>What is web gl? & three js</h2>

Web gl is a javascript API for rendering 2D and 3D grafics in web browser. Same can three js do, but three js is a library on top of web gl. It means three js is a collection of tools and functions that sit on top of web gl and make it easier to use. Because three js have methods and features of specific tasks.

<h2 style='color: aquamarine;' align='center'>Making a cube as quick as possible</h2>

In this step we setup three js and also setup basic scene, camera and renderer, With the help of documentation we create a cube.

<h3 style='color: aqua;'>Setup Three JS</h3>


1. Create a new html file, and paste simple template.
2. Install three js from cdn, paste it just before script tag. 
     ```html 
     <script src="https://cdn.jsdelivr.net/npm/three@0.150.0/build/three.min.js"></script>
     ```
3. Create script file and import it in html file.
4. Configure tailwind with cdn. And paste it just below the title.
    ```html
    <script src="https://cdn.tailwindcss.com"></script>
    ```
5. create a `canvas` and give it id.
    ```html
    <canvas id="bg"></canvas>
    ```
6. In script tag initialize three js.
7. Go to three js documentation and copy paste the code of cube.
8. Click on create a scene, and create a scene.
    ```javascript
    import * as THREE from 'three';
    <!-- While using cdn we do not need to write this -->

    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

    <!-- Gap 1 -->
    const renderer = new THREE.WebGLRenderer();
    renderer.setSize( window.innerWidth, window.innerHeight );
    document.body.appendChild( renderer.domElement );
    ```
9. Copy second part of code and paste it in `gap 1`.
    ```javascript
    const geometry = new THREE.BoxGeometry( 1, 1, 1 );
    const material = new THREE.MeshBasicMaterial( { color: 0x00ff00 } );
    const cube = new THREE.Mesh( geometry, material );
    scene.add( cube );

    camera.position.z = 5;
    ```
10. Copy Rendering the scene code and paste it below the above code.
    ```javascript
    function animate() {
	    renderer.render( scene, camera );

    }

    renderer.setAnimationLoop( animate );
    ```
11. Animating the cube.
    ```javascript
    function animate() {

	    renderer.render( scene, camera );
        cube.rotation.x += 0.01;
	    cube.rotation.y += 0.01;
    }

    renderer.setAnimationLoop( animate );
    ```
12. Now, perform some changes in code and see the results.
    ```javascript
    const canvas = document.querySelector('#bg');
    const renderer = new THREE.WebGLRenderer({canvas: canvas});

    <!-- Remove -->
    document.body.appendChild( renderer.domElement );
    <!-- Remove -->
    renderer.setAnimationLoop( animate );
    <!-- And add in animate function -->
    window.requestAnimationFrame(animate);
    <!-- Now, run the function -->
    animate();
    
    ```
<h2 style='color: aquamarine;' align='center'>Understanding the parts</h2>

Every time we use three js we need some basic things. Everything in three js is an object.

1. **Scene :** 
    - It is a container that holds all the objects, camera and lights.
    - The 3d world that we see in the browser is inside the scene. It means, everything that we see in the browser is inside the scene.
        ```javascript
        const scene = new THREE.Scene();
        ```

2. **Camera :**
    - It is used to view the scene.
    - Camera means, from where we will see the scene. Because scene is everthing which is in browser.
        ```javascript
        const camera = new THREE.PerspectiveCamera(65, window.innerWidth / window.innerHeight, 0.1, 100);
        scene.add(camera);
        ```
3. **Renderer :**
    - It is used to render the scene.
    - It is used to display the scene in the browser.
    ```javascript
    const renderer = new THREE.WebGLRenderer();
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.body.appendChild(renderer.domElement);
    renderer.render(scene, camera);
    ```
4. **Geometry :** 
    - It is used to create the shape of the object.
        ```javascript
        const geometry = new THREE.BoxGeometry(1, 1, 1);
        ```
5. **Material :**
    - It is used to give the color to the object.
        ```javascript
        const material = new THREE.MeshBasicMaterial({color: 0x00ff00});
        ```
6. **Mesh :**
    - It is used to create the object.
    - It is a combination of geometry and material.
        ```javascript
        const mesh = new THREE.Mesh(geometry, material);
        scene.add(mesh);
        ```
7. **Request Animation Frame :**
    - It is used to animate the object.
        ```javascript
        function animate() {
            window.requestAnimationFrame(animate);
            renderer.render(scene, camera);
            cube.rotation.x += 0.01;
            cube.rotation.y += 0.01;
        }
        animate();
        ```

<h3 style='color: aqua;'>Position, Rotation, Scale</h3>

**Position** is a property of object. It is used to set the position of the object. And also I want to define the axis in three JS.<br />

```javascript
    mesh.position.set(0, 0, 0);
    mesh.position.x = 2;
```

**Rotation** is a property of object. It is used to set the rotation of the object.<br />

```javascript
    mesh.rotation.set(0, 0, 0);
    mesh.rotation.x = 2;
```

**Scale** is a property of object. It is used to set the scale of the object. scale means size of object.

```javascript
    mesh.scale.set(1, 1, 1);
    mesh.scale.x = 2;
```


1. **x-axis :** It is the horizontal axis.
2. **y-axis :** It is the vertical axis.
3. **z-axis :** It is the depth axis.   

> So, lastly we have to add mesh into scene.
```javascript
    scene.add(mesh);
```
<h3 style='color: aqua;'>Math PI</h3>

When we rotate a value at `Math.PI`. It means it moves `180` degrees. So, let's use it a little:

```javascript
mesh.rotation.x = Math.PI * 2;
// It means 360 degrees
mesh.rotation.x = Math.PI / 2;
// It means 90 degree

```
<h3 style='color: aqua;'>Clock</h3>

Clock is used to get the time. It is used to animate the object.

```javascript
const clock = new THREE.Clock();
const elapsedTime = clock.getElapsedTime();

function animate() {
    const elapsedTime = clock.getElapsedTime();
    renderer.render(scene, camera);
    cube.rotation.y += elapsedTime * 2;
    cube.rotation.z += elapsedTime;
}

renderer.setAnimationLoop(animate);
```




<h2 style='color: aquamarine;' align='center'>Transformations</h2>
<h2 style='color: aquamarine;' align='center'>Setting up vite</h2>

In the tutorial harsh sharma use plain vite, but I will use React. Because I already now it.<br />

**Steps :**

1. instal vite, install tailwind, setup properly
2. Install three js for React. Search on ChatGPT and follow the installation instructions.
3. Repeat the same steps which we have done in making cube.


<h2 style='color: aquamarine;' align='center'>Making responsive</h2>

I do not learn that, how our 3d model will react on resize. Just I learn a problem solution. That when we resize the window, then according to the resize we can not be able to see the 3d model. So, we need to set the size of the canvas according to the window.

```javascript
    window.addEventListener('resize', () => {
      renderer.setSize(window.innerWidth, window.innerHeight);
      camera.aspect = window.innerWidth / window.innerHeight;
     //   Whenever we aspect the camera we have to updateProjectionMatix
      camera.updateProjectionMatrix();
    })
```

<h2 style='color: aquamarine;' align='center'>Orbit Controls</h2>

Orbit controls are the controls which are used to rotate the camera around the object. <br />
For read more about Orbit controls, [click here](https://threejs.org/docs/index.html?q=orbit#examples/en/controls/OrbitControls). So let's see how to use it.

1. Import Orbit controls from three js.
    ```javascript
    import { OrbitControls } from 'three/addons/controls/OrbitControls.js';
    ```
2. Create a new instance of Orbit controls.
    ```javascript
    const controls = new OrbitControls(camera, renderer.domElement);
    ```
3. Now, update the controls in the animate function for keep updating the controls.
    ```javascript
    controls.update();
    // And add it in animate function.
    ```
> And here are some other controls which we can use

- controls.enableDamping = true; // It is used to smooth the rotation of the camera.
- controls.dampingFactor = 0.25; // It is used to set the speed of the rotation of the camera.
- controls.enableZoom = true; // It is used to enable the zoom of the camera.

> And there is a lot for Orbit controls. Read more about it [here](https://threejs.org/docs/index.html?q=orbit#examples/en/controls/OrbitControls).

<h2 style='color: aquamarine;' align='center'>Geometries</h2>

Geometry is a shape of object. It is used to create the shape of the object. It is the skeleton of the object. There are many types of geometries in three js. And here you can explore all of them [here](https://threejs.org/docs/index.html?q=geometry#api/en/geometries/BoxGeometry).

whenever we use a geometry we need to add it in the scene. Just like we add cube geometry in the scene. Geometry is a class and when we create an object using that class, it is an instance. And also, the connstructor get some values. For example:

```javascript
    const geometry = new THREE.BoxGeometry(1, 1, 1);
    // Here, 1, 1, 1 is the size of the cube.
```

<h2 style='color: aquamarine;' align='center'>Materials</h2>

Materials in three js are used to give the color to the object. It is used to give the texture to the object. It is used to give the material to the object. There are many types of materials in three js. And here you can explore all of them [here](https://threejs.org/docs/index.html?q=material#api/en/materials/MeshBasicMaterial).

whenever we use a material we need to add it in the scene. Just like we add cube material in the scene. Material is a class and when we create an object using that class, it is an instance. And also, the connstructor get some values. For example:

```javascript
    const material = new THREE.MeshBasicMaterial({color: 0x00ff00});
    // Here, 0x00ff00 is the color of the material.
```



<h2 style='color: aquamarine;' align='center'>Textures</h2>

Textures basically means, we can download a color or image and we can put it on our 3d object. This is what I learn in the video, I also download a texture from google and apply on box, code is in `TheeWithReact`.

```javascript
    const texture = new THREE.TextureLoader();
    const color = texture.load('./texture/color.jpg');
    const normal = texture.load('./texture/normal.png');
    const roughness = texture.load('./texture/roughness.jpg');
    // Now, we have to pass this texture in material.
    const material = new THREE.MeshStandardMaterial({
      map: color,
      roughnessMap : roughness,
      normalMap : normal,
    });
```

<h2 style='color: aquamarine;' align='center'>lil-gui</h2>

lil-gui is a external library which provide us the functionality of create a GUI(Grafical User Interface) of controls which three js provide us for controlling the object. Here is how we can use it:

1. Install lil-gui from npm.
    ```javascript
    npm install lil-gui
    ```
2. Import lil-gui in our file.
    ```javascript
    import GUI from 'lil-gui';
    ```
3. Then, ask to ai for creating a gui.
    ```javascript
    write code of lil-gui for controlling the object. And create material and mesh folder.
    ```
4. And here is the code which ai give me.

    ```javascript

    // Material folder
    const materialFolder = gui.addFolder('Material');
    materialFolder.add(material, 'wireframe');
    materialFolder.addColor(material, 'color');
    materialFolder.add(material, 'metalness', 0, 1, 0.01);
    materialFolder.add(material, 'roughness', 0, 1, 0.01);

    // Mesh folder
    const meshFolder = gui.addFolder('Mesh');
    meshFolder.add(cube.position, 'x', -3, 3, 0.01);
    meshFolder.add(cube.position, 'y', -3, 3, 0.01);
    meshFolder.add(cube.position, 'z', -3, 3, 0.01);
    meshFolder.add(cube.rotation, 'x', 0, Math.PI * 2, 0.01);
    meshFolder.add(cube.rotation, 'y', 0, Math.PI * 2, 0.01);
    meshFolder.add(cube.rotation, 'z', 0, Math.PI * 2, 0.01);
    meshFolder.add(cube.scale, 'x', 0.1, 2, 0.01);
    meshFolder.add(cube.scale, 'y', 0.1, 2, 0.01);
    meshFolder.add(cube.scale, 'z', 0.1, 2, 0.01);
    
    ```

<h2 style='color: aquamarine;' align='center'>Lights</h2>

Understand the lights in such a way, that if there is no light in the world, We will not be able to see the objects of the world. Same concept in three js, If we do not put light in the scene. We will see nothing. <br />
So, secondly we have eight lights, which three js provide us. According to hitesh sharma sir, we will maximum time we use 3 of them. [Read More](https://threejs.org/docs/?q=light#api/en/lights).

1. **AmbientLight :** It will spread all around the object.
2. **DirectLight :** It comes from a direction.
3. **PointLight :** Point light comes form a point.

How to write code of it:

```javascript
let ambient = new THREE.AmbientLight(white, 1);
scene.add(ambient);
// First argument is color, and second argument is quantity of light
let directionalLight = new THREE.DirectionalLight(white, 1)
directionalLight.position.set(10, 10, 10);
// x-axis, y-axis, z-axis
scene.add(directionalLight);

let pointLight = new THREE.PointLight(white, 1, 100, 2)
pointLight.position.set(10, 10, 10);
scene.add(pointLight);
```

> We can also view the lights in lil-gui panel by giving the prompt `add lil-gui panel for lights`.

<h3 style='color: aqua;'>Helpers</h3>

Helpers help us to see the lights in the scene. There are many helpers in three js. And here you can explore all of them [here](https://threejs.org/docs/index.html?q=helper#api/en/helpers/AmbientLightHelper).

```javascript
const light = new THREE.DirectionalLight( 0xFFFFFF );
scene.add( light );

const helper = new THREE.DirectionalLightHelper( light, 5 );
scene.add( helper );

```


<h2 style='color: aquamarine;' align='center'>Adding 3d models</h2>

We can add 3d models in three js in two ways:

1. **Using Blender:** We can create a 3d model in blender and then we can import it in three js.
2. **Using three js editor:** We can create a 3d model in three js editor and then we can import it in three js.





