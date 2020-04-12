<script>
    import Header from './Header.svelte';
    import Footer from './Footer.svelte';
    import MainSection from './MainSection.svelte';
    import Design from './contents/Design.svelte';
    import Library from './contents/Library.svelte';
    import Templates from './contents/Templates.svelte';
    import Illustrations from './contents/Illustrations.svelte';
    import TemplatesNews from './contents/TemplatesNews.svelte';
    import Components from './contents/Components.svelte';
</script>

<main>
    <Header />
    <MainSection />

    <Design />
    <Library />
    <Templates />
    <Illustrations />
    <TemplatesNews />
    <Components />

    <Footer />
</main>

<style lang="scss">
    @import '../_sources/styles/mixins.scss';

    main {
        overflow-x: hidden;
        min-width: 320px;
        margin: auto;

        @include responsive(large) {

        }
        @include responsive(medium) {
        }
        @include responsive(small) {
        }
    }
</style>
