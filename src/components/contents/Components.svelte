<script>
    import ContentSection from './../ContentSection.svelte';

    const images = [
        'components/components1.png',
        'components/components2.png',
        'components/components3.png',
        'components/components4.png',
    ];
</script>

<section>
    <ContentSection
            title="Components"
            desc="A huge symbols library for creating your own components.<br> There are all necessary components for even complex cases."
    >

        <div class="gif" data-aos="zoom-in">
            <img src="/images/components/gif_components.gif" alt="components-gif">
        </div>

        <div class="images" data-aos="zoom-in">
            {#each images as img, index}
                <img src={`/images/${img}`} alt={`components-${index}`}>
            {/each}
        </div>
    </ContentSection>
</section>

<style lang="scss">
    @import "../../_sources/styles/mixins";

    section {
        background: url("/images/components/bg_components.svg");
        background-size: cover;

        @include responsive(large) {
            padding: 122px 0 274px;
        }

        @include responsive(medium) {
            padding: 80px 0 255px;
        }

        @include responsive(small) {
            padding: 60px 0 165px;
        }
    }

    .gif {
        width: 120%;
        position: relative;
        left: -10%;

        @include responsive(large) {
            margin-bottom: 14px;
        }

        @include responsive(medium) {
            margin-bottom: 8px;
        }

        @include responsive(small) {
            margin-bottom: 8px;
        }
    }

    .images {
        img {
            &:nth-child(2) {
                margin-top: -20%;
            }

            &:nth-child(3), &:nth-child(4) {
                margin-top: -23%;
            }
        }
    }
</style>
