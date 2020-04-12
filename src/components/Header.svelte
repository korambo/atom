<script>
    import Button from './Button.svelte';
    import Logo from './../_sources/icons/logo.svg';
</script>

<header>
    <div class="logo">
        <a href="http://the18.design">
            {@html Logo}
        </a>
    </div>

    <div class="buttons">
        <Button text="Preview" primary url="https://www.dropbox.com/sh/mdn4urz2a91jfz4/AADaqhWf4d6Oyutpbaxd2elBa?dl=0" />
        <Button text="Download" url="https://gumroad.com/l/OcePo" />
    </div>
</header>

<style lang="scss">
    @import "../_sources/styles/mixins";

    header {
        position: fixed;
        left: 0;
        right: 0;
        display: flex;
        justify-content: space-between;
        z-index: 2;

        @include responsive(large) {
            padding: 40px;
        }
        @include responsive(medium) {
            padding: 28px;
        }
        @include responsive(small) {
            padding: 14px;
        }
    }

    .logo {
        width: 40px;
    }

    @include responsive(small) {
        .buttons {
            display: none;
        }
    }
</style>
