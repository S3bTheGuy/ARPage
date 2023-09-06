<script>

</script>

<svelte:head>
	<title>icon1</title>
	<meta name="description" content="icon1" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <script async src="https://unpkg.com/es-module-shims@1.7.3/dist/es-module-shims.js"></script>
    <script type="importmap">
      {
        "imports": {
      "three": "https://unpkg.com/three@0.153.0/build/three.module.js",
      "three/addons/": "https://unpkg.com/three@0.153.0/examples/jsm/",
      "mindar-image-three":"https://cdn.jsdelivr.net/npm/mind-ar@1.2.2/dist/mindar-image-three.prod.js"
        }
      }
      </script>
      <script type="module">
        import * as THREE from 'three';
        import { MindARThree } from 'mindar-image-three';
        const mindarThree = new MindARThree({
      container: document.querySelector("#container"),
      imageTargetSrc: "../../lib/targets.mind"
        });
        const {renderer, scene, camera} = mindarThree;
        const anchor = mindarThree.addAnchor(0);
        const geometry = new THREE.PlaneGeometry(1, 0.55);
        const material = new THREE.MeshBasicMaterial( {color: 0x00ffff, transparent: true, opacity: 0.5} );
        const plane = new THREE.Mesh( geometry, material );
        anchor.group.add(plane);
        const start = async() => {
      await mindarThree.start();
      renderer.setAnimationLoop(() => {
        renderer.render(scene, camera);
      });
        }
        const startButton = document.querySelector("#startButton");
        startButton.addEventListener("click", () => {
      start();
        });
        stopButton.addEventListener("click", () => {
      mindarThree.stop();
      mindarThree.renderer.setAnimationLoop(null);
        });
      </script>
</svelte:head>

<section>
  <div id="control">
    <button id="startButton">Start</button>
    <button id="stopButton">Stop</button>
  </div>
  <div id="container">
  </div>
</section>

<style>

.arjs-loader {
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 9999;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .arjs-loader div {
    text-align: center;
    font-size: 1.25em;
    color: white;
  }
</style>