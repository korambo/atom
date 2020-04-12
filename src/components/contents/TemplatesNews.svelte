<script>
    import ContentSection from './../ContentSection.svelte';

    const images = [
        'templates_news/templates_news1.png',
        'templates_news/templates_news2.png',
        'templates_news/templates_news3.png',
        'templates_news/templates_news4.png',
    ];
</script>

<section>
    <ContentSection
            title="Templates<br> for news feed"
            desc="Special cards for news feed will let you be<br> creative with your press release or articles."
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
            padding: 126px 0 252px;
        }

        @include responsive(medium) {
            padding: 39px 0 121px;
        }

        @include responsive(small) {
            padding: 42px 0 82px;
        }
    }

    .images img {
        @include responsive(large) {
            margin-bottom: 20px;
        }

        @include responsive(medium) {
            margin-bottom: 24px;
        }

        @include responsive(small) {
            margin-bottom: 10px;
        }

        &:last-child {
            margin-bottom: 0;
        }
    }
</style>
