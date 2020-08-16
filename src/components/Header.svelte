<script>
    import Button from './Button.svelte';
    import Logo from './../_sources/icons/logo.svg';
    window.$crisp=[];window.CRISP_WEBSITE_ID="d58fce8c-3191-4b3f-bdb3-769f6839e75f";(function(){d=document;s=d.createElement("script");s.src="https://client.crisp.chat/l.js";s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})();
    Paddle.Setup({ vendor: 112127 });
</script>

<header>
    <div class="logo">
        <a href="http://the18.design">
            {@html Logo}
        </a>
    </div>

    <div class="buttons">
        <Button text="Preview" primary url="https://www.dropbox.com/sh/mdn4urz2a91jfz4/AADaqhWf4d6Oyutpbaxd2elBa?dl=0" />
        <Button text="Purchase" id="buy" />
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


<script src="https://cdn.paddle.com/paddle/paddle.js"></script>
