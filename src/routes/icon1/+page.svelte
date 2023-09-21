<script>

</script>

<svelte:head>
	<title>icon1</title>
	<meta name="description" content="icon1" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar-nft.js"></script>
    </svelte:head>

<section>
  <div class="arjs-loader">
    <div>Loading, please wait...</div>
  </div>


  <!--AFRAME SCENE-->
  <a-scene
    vr-mode-ui="enabled: false;"
    renderer="logarithmicDepthBuffer: true;"
    embedded
    arjs="trackingMethod: best; sourceType: webcam;debugUIEnabled: false;"
  >
  <!-- THE NFT IMAGE USED FOR TRACKING-->
  <a-nft
    type="nft"
    url="/lib/no1"
    smooth="true"
    smoothCount="10"
    smoothTolerance=".01"
    smoothThreshold="5"
  >
  <!-- DEFINE GLTF Model -->
  <a-entity
    gltf-model="/lib/bottleLarge.gltf"
    scale="5 5 5"
    position="50 150 0"
  >
  </a-entity>
  </a-nft>
  <!-- camera -->
  <a-entity camera></a-entity>
  </a-scene>
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