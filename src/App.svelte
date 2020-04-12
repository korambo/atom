<script>
	import Layout from './components/Layout.svelte';
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
