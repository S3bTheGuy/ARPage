<script lang="ts">
    import welcome from '$lib/images/svelte-welcome.webp';
    import welcome_fallback from '$lib/images/svelte-welcome.png';
    // they range from 01 to 17
    import E_SDG_Icons_01 from '../lib/images/E_SDG_Icons-01.jpg';
    import E_SDG_Icons_02 from '../lib/images/E_SDG_Icons-02.jpg';
    import E_SDG_Icons_03 from '../lib/images/E_SDG_Icons-03.jpg';
    import E_SDG_Icons_04 from '../lib/images/E_SDG_Icons-04.jpg';
    import E_SDG_Icons_05 from '../lib/images/E_SDG_Icons-05.jpg';
    import E_SDG_Icons_06 from '../lib/images/E_SDG_Icons-06.jpg';
    import E_SDG_Icons_07 from '../lib/images/E_SDG_Icons-07.jpg';
    import E_SDG_Icons_08 from '../lib/images/E_SDG_Icons-08.jpg';
    import E_SDG_Icons_09 from '../lib/images/E_SDG_Icons-09.jpg';
    import E_SDG_Icons_10 from '../lib/images/E_SDG_Icons-10.jpg';
    import E_SDG_Icons_11 from '../lib/images/E_SDG_Icons-11.jpg';
    import E_SDG_Icons_12 from '../lib/images/E_SDG_Icons-12.jpg';
    import E_SDG_Icons_13 from '../lib/images/E_SDG_Icons-13.jpg';
    import E_SDG_Icons_14 from '../lib/images/E_SDG_Icons-14.jpg';
    import E_SDG_Icons_15 from '../lib/images/E_SDG_Icons-15.jpg';
    import E_SDG_Icons_16 from '../lib/images/E_SDG_Icons-16.jpg';
    import E_SDG_Icons_17 from '../lib/images/E_SDG_Icons-17.jpg';

</script>

<svelte:head>
    <title>Hjem</title>
    <meta name="description" content="Svelte demo app"/>
    <script src="https://cdn.jsdelivr.net/gh/hiukim/mind-ar-js@1.2.2/dist/mindar-image.prod.js"></script>
    <script src="https://aframe.io/releases/1.4.2/aframe.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/donmccurdy/aframe-extras@v6.1.1/dist/aframe-extras.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/hiukim/mind-ar-js@1.2.2/dist/mindar-image.aframe.js"></script>
</svelte:head>

<section>

    <a-scene mindar-image="imageTargetSrc: ../lib/targets.mind;" color-space="sRGB" renderer="colorManagement: true, physicallyCorrectLights">
        <a-assets>
            <img id="card" src="https://cdn.jsdelivr.net/gh/hiukim/mind-ar-js@1.2.2/examples/image-tracking/assets/card-example/card.png" />
            <a-asset-item id="avatarModel" src="https://cdn.jsdelivr.net/gh/hiukim/mind-ar-js@1.2.2/examples/image-tracking/assets/card-example/softmind/scene.gltf"></a-asset-item>
          </a-assets>
    
    
          <a-camera position="0 0 0" look-controls="enabled: false"></a-camera>
    
    
          <a-entity mindar-image-target="targetIndex: 0">
            <a-plane src="#card" position="0 0 0" height="0.552" width="1" rotation="0 0 0"></a-plane>
            <a-gltf-model rotation="0 0 0 " position="0 0 0.1" scale="0.005 0.005 0.005" src="#avatarModel" animation="property: position; to: 0 0.1 0.1; dur: 1000; easing: easeInOutQuad; loop: true; dir: alternate">
          </a-entity>
    </a-scene>
    <h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp"/>
				<img src={welcome_fallback} alt="Welcome"/>
			</picture>
		</span>

        Lars<br/>
    </h1>

    <h2>
        Gotta add some content here
    </h2>

    <div class="grid-container">
        <div class="grid-row">
            <img src={E_SDG_Icons_01} alt="Goal 1"/>
            <img src={E_SDG_Icons_02} alt="Goal 2"/>
            <img src={E_SDG_Icons_03} alt="Goal 3"/>
        </div>
        <div class="grid-row">
            <img src={E_SDG_Icons_04} alt="Goal 4"/>
            <img src={E_SDG_Icons_05} alt="Goal 5"/>
            <img src={E_SDG_Icons_06} alt="Goal 6"/>
        </div>
        <div class="grid-row">
            <img src={E_SDG_Icons_07} alt="Goal 7"/>
            <img src={E_SDG_Icons_08} alt="Goal 8"/>
            <img src={E_SDG_Icons_09} alt="Goal 9"/>
        </div>
        <div class="grid-row">
            <img src={E_SDG_Icons_10} alt="Goal 10"/>
            <img src={E_SDG_Icons_11} alt="Goal 11"/>
            <img src={E_SDG_Icons_12} alt="Goal 12"/>
        </div>
        <div class="grid-row">
            <img src={E_SDG_Icons_13} alt="Goal 13"/>
            <img src={E_SDG_Icons_14} alt="Goal 14"/>
            <img src={E_SDG_Icons_15} alt="Goal 15"/>
        </div>
        <div class="grid-row">
            <img src={E_SDG_Icons_16} alt="Goal 16"/>
            <img src={E_SDG_Icons_17} alt="Goal 17"/>
            <div>
            <svg class="logo" version="1.1" id="logo" xmlns="http://www.w3.org/2000/svg"
                 xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="60px" height="31px"
                 viewBox="0 0 60 31" style="enable-background: new 0 0 60 31;" xml:space="preserve">
				<polygon class="st1"
                         points="18.7,0.7 0.4,0.7 0.4,8.5 7.1,8.5 0.4,15.5 0.4,30.4 18.7,30.4 18.7,22.6 5,22.6 18.7,8.1 "></polygon>
                <path class="st1" d="M36.1,15.5L36.1,15.5L36.1,15.5c2.5-1.4,3.3-4.1,3.3-6.5c0-4.2-3.2-8.4-9.4-8.4h-8.8v7.8h5.5h0.9H29
				  c1.4,0,2.1,1.1,2.1,2.2s-0.7,2.2-2.1,2.2h-1.4h-0.9h-5.5v2.8v2.8h5.5h0.9H29c1.4,0,2.1,1.1,2.1,2.2s-0.7,2.2-2.1,2.2h-1.4h-0.9h-5.5
				  v7.8H30c6.2,0,9.4-4.2,9.4-8.4C39.4,19.6,38.5,16.9,36.1,15.5z"></path>
                <path id="Upper_c" class="st1" d="M46.4,8.1c2.9,0,5.1,1.9,5.8,4.4h0.5L59.7,7C57,2.8,52.3,0.1,46.4,0.1c-1.6,0-3.2,0.2-4.7,0.7v9.3
				  C42.9,8.8,44.5,8.1,46.4,8.1z"></path>
                <path class="st1" d="M52.8,18.4h-0.5c-0.7,2.6-2.9,4.4-5.9,4.4c-2,0-3.6-0.8-4.7-2v9.3c1.5,0.4,3.1,0.7,4.7,0.7
				  c5.7,0,10.7-2.8,13.4-7.2L52.8,18.4z"></path>
			  </svg>
            </div>
        </div>
    </div>

</section>

<style>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        flex: 0.6;
    }

    h1 {
        width: 100%;
    }

    .welcome {
        display: block;
        position: relative;
        width: 100%;
        height: 0;
        padding: 0 0 calc(100% * 495 / 2048) 0;
    }

    .welcome img {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        display: block;
    }


    .grid-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        padding: 20px;
    }

    .grid-row {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        justify-content: center;
        gap: 10px;
        margin: 10px 0;
        width: 100%;
    }

    .grid-row img {
        max-width: 100%;
        height: auto;
    }

    .st1 {
        fill: #FFFFFF;
        margin: 0;
    }

    /* logo for phone screens */
    .logo {
        width: 100%;
        height: 100%;
        align-items: center;
        background-color: black;
        display: block;
        margin: 0 auto;
    }

    /*
    for screens larger than 768px wide
    */
    @media screen and (min-width: 768px) {
        .grid-container {
            flex-direction: row;
            flex-wrap: wrap;
        }

        .grid-row {
            margin: 10px;
        }

        .logo {
            width: 100%;
            height: 100%;
            align-items: center;
            background-color: black;
            display: block;
            margin: 0 auto;
        }
    }
</style>
