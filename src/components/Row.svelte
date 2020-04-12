<script>
    import cn from 'classnames';

    export let disable = false;
</script>

<div class={cn({ row: !disable })}>
    <slot />
</div>

<style lang="scss">
    @import "../_sources/styles/mixins";

    .row {
        max-width: 1440px;
        margin: auto;

        @include responsive(large) {
            padding: 0 220px;
        }
        @include responsive(medium) {
            padding: 0 50px;
        }
        @include responsive(small) {
            padding: 0 20px;
        }
    }
</style>
