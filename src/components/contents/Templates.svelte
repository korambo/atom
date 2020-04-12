<script>
    import ContentSection from './../ContentSection.svelte';

    const images = [
        'templates/templates1.png',
        'templates/templates2.png',
        'templates/templates3.png',
        'templates/templates4.png',
        'templates/templates5.png',
        'templates/templates6.png',
        'templates/templates7.png',
    ];
</script>

<section>
    <ContentSection
            title="Templates"
            desc="Use simple and handy cards system.<br> It can be easily scaled to any app or tool you need."
    >
        <div class="images">
            {#each images as img, index}
                <img src={`/images/${img}`} alt={`template_news-${index}`}>
            {/each}
        </div>
    </ContentSection>
</section>

<style lang="scss">
    @import "../../_sources/styles/mixins";

    section {
        @include responsive(large) {
            padding: 55px 0 194px;
        }

        @include responsive(medium) {
            padding: 125px 0 72px;
        }

        @include responsive(small) {
            padding: 31px 0 111px;
        }
    }

    .images img {
        @include responsive(large) {
            margin-bottom: 20px;
        }

        @include responsive(medium) {
            margin-bottom: 9px;
        }

        @include responsive(small) {
            margin-bottom: 5px;
        }

        &:last-child {
            margin-bottom: 0;
        }
    }
</style>
