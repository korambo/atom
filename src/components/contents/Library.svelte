<script>
    import ContentSection from './../ContentSection.svelte';
</script>

<section>
    <ContentSection
            title="Library will help<br> you to beeffective"
            desc="Don't waste your time on developing components,<br> you can use customizable and flexible UI KIT."
    >
        <img class="gif" src="/images/library/gif_library.gif" alt="gif_library">
    </ContentSection>
</section>

<style lang="scss">
    @import "../../_sources/styles/mixins";

    .gif {
        width: 120%;
        position: relative;
        left: -10%;
    }

    section {
        background: url("/images/library/bg_library.svg");
        background-size: cover;

        @include responsive(large) {
            padding: 390px 0 318px;
        }

        @include responsive(medium) {
            padding: 266px 0 218px;
        }

        @include responsive(small) {
            padding: 165px 0 135px;
        }
    }
</style>
