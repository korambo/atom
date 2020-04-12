<script>
    import ContentSection from './../ContentSection.svelte';
</script>

<section>
    <ContentSection
            title="Design"
            desc="Simple and light design for your ideas and creativity.<br> You can use UI Kit to create your own web pages and solutions."
    >
        <img src="/images/design/design.png" alt="design">
    </ContentSection>
</section>

<style lang="scss">
    @import "../../_sources/styles/mixins";

    section {
        @include responsive(large) {
            margin-bottom: -90px;
        }
        @include responsive(medium) {
            margin-bottom: -126px;
        }
        @include responsive(small) {
            margin-bottom: -30px;
        }
    }
</style>
