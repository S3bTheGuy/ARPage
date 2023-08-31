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
	import ZBC_logo from '../lib/images/ZBC_logo.png';

	// import View3D from "@egjs/svelte-view3d";
</script>

<svelte:head>
	<title>Hjem</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<!-- View3D causes erros since it is not SSR compatible.

	<View3D src="/egjs-view3d/model/draco/alarm.glb"
			iosSrc="/egjs-view3d/model/usdz/alarm.usdz"
			webAR={true} />
-->
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		Lars<br />
	</h1>

	<h2>
		Gotta add some content here
	</h2>

	<div class="grid-container">
		<div class="grid-row">
			<img src={E_SDG_Icons_01} alt="Goal 1" />
			<img src={E_SDG_Icons_02} alt="Goal 2" />
			<img src={E_SDG_Icons_03} alt="Goal 3" />
		</div>
		<div class="grid-row">
			<img src={E_SDG_Icons_04} alt="Goal 4" />
			<img src={E_SDG_Icons_05} alt="Goal 5" />
			<img src={E_SDG_Icons_06} alt="Goal 6" />
		</div>
		<div class="grid-row">
			<img src={E_SDG_Icons_07} alt="Goal 7" />
			<img src={E_SDG_Icons_08} alt="Goal 8" />
			<img src={E_SDG_Icons_09} alt="Goal 9" />
		</div>
		<div class="grid-row">
			<img src={E_SDG_Icons_10} alt="Goal 10" />
			<img src={E_SDG_Icons_11} alt="Goal 11" />
			<img src={E_SDG_Icons_12} alt="Goal 12" />
		</div>
		<div class="grid-row">
			<img src={E_SDG_Icons_13} alt="Goal 13" />
			<img src={E_SDG_Icons_14} alt="Goal 14" />
			<img src={E_SDG_Icons_15} alt="Goal 15" />
		</div>
		<div class="grid-row">
			<img src={E_SDG_Icons_16} alt="Goal 16" />
			<img src={E_SDG_Icons_17} alt="Goal 17" />
			<img src={ZBC_logo} alt="ZBC logo" />
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
    }
</style>
