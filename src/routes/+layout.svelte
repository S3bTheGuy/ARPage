<script>
	import { browser } from '$app/environment';
	import { page } from '$app/stores';
	import { webVitals } from '$lib/vitals';
	import Header from './Header.svelte';
	import './styles.css';
	import { dev } from '$app/environment';
	import { inject } from '@vercel/analytics';

	inject({ mode: dev ? 'development' : 'production' });

	/** @type {import('./$types').LayoutServerData} */
	export let data;

	$: if (browser && data?.analyticsId) {
		webVitals({
			path: $page.url.pathname,
			params: $page.params,
			analyticsId: data.analyticsId
		});
	}
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>Lavet Med Svelte <br /> Mikkel M. H. Pedersen & Sebastian F. Steffensen</p>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
        text-align: center;
        padding: 12px;
        background-color: #e6e9ef;
        border-top: 1px solid #4c4f69;
    }

    footer p {
        margin: 0;
        font-size: 14px;
		font-weight: 800;
    }

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
