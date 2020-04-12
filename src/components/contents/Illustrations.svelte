<script>
    import ContentSection from './../ContentSection.svelte';

    const images = [
        'illustrations/illustrations1.png',
        'illustrations/illustrations2.png',
        'illustrations/illustrations3.png',
        'illustrations/illustrations4.png',
    ];
</script>

<section>
    <ContentSection
            title="Illustrations"
            desc="With illustration cards, you will create<br> news feeds or presentations."
    >
        <div class="images">
            {#each images as img, index}
                <img src={`/images/${img}`} alt={`illustrations-${index}`} data-aos="zoom-in">
            {/each}
        </div>
    </ContentSection>
</section>

<style lang="scss">
    @import "../../_sources/styles/mixins";

    section {
        background: url("/images/illustrations/bg_illustrations.svg");
        background-size: cover;

        @include responsive(large) {
            padding: 180px 0 172px;
        }

        @include responsive(medium) {
            padding: 129px 0 101px;
        }

        @include responsive(small) {
            padding: 80px 0 93px;
        }
    }

    .images img {
        @include responsive(large) {
            margin-bottom: 40px;
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
