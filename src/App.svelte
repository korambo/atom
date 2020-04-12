<script>
	import { onMount } from 'svelte';
	import AOS from 'aos';
	import 'aos/dist/aos.css';

	import Layout from './components/Layout.svelte';

	onMount(() => {
		AOS.init({
			duration: 1000
		});
	});
</script>

<Layout name="123"/>

<style lang="scss">
	@import "_sources/styles/fonts";
	@import "_sources/styles/variables";

	:global(body) {
		width: 100%;
		padding: 0;
		background-color: $background-color;
	}
</style>
