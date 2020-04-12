<script>
    import Row from './Row.svelte';

    export let title = '';
    export let desc = '';
    export let withoutPadding = false;
</script>

<div class="content">
    <Row disable={withoutPadding}>
        <div class="text">
            <h3 class="title">{@html title}</h3>
            <p class="desc">{@html desc}</p>
        </div>
        <slot />
    </Row>
</div>

<style lang="scss">
    @import "../_sources/styles/variables";
    @import "../_sources/styles/mixins";

    .title {
        font-weight: bold;
        color: $text-color2;

        @include responsive(large) {
            font-size: 84px;
            line-height: 76px;
            letter-spacing: -1.8px;
            margin-bottom: 20px;
        }

        @include responsive(medium) {
            text-align: center;
            font-size: 68px;
            line-height: 60px;
            letter-spacing: -1px;
            margin-bottom: 16px;
        }

        @include responsive(small) {
            text-align: center;
            font-size: 32px;
            line-height: 32px;
            letter-spacing: -0.5px;
            margin: 0 auto 14px;
        }

        @media (max-width: 567px) {
            :global(br) {
                display: none;
            }
        }
    }

    .desc {
        font-weight: 500;
        color: $text-color2;

        @include responsive(large) {
            font-size: 20px;
            line-height: 30px;
            letter-spacing: 0.2px;
            margin-bottom: 60px;
        }

        @include responsive(medium) {
            text-align: center;
            font-size: 16px;
            line-height: 24px;
            letter-spacing: 0.2px;
            margin-bottom: 32px;
        }

        @include responsive(small) {
            text-align: center;
            font-size: 16px;
            line-height: 24px;
            letter-spacing: 0.2px;
            margin-bottom: 25px;
        }

        @media (max-width: 567px) {
            :global(br) {
                display: none;
            }
        }
    }
</style>
