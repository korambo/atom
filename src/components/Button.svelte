<script>
    import cn from 'classnames';

    export let text = '';
    export let url = '';
    export let primary;
    export let type = 'normal';

    const classNames = cn({
        'primary': primary,
        'normal': type === 'normal',
        'full': type === 'full',
    });
</script>

<button class={classNames}>
    <a href={url} target="_blank">{text}</a>
</button>

<style lang="scss">
    @import "./../_sources/styles/variables";
    @import "./../_sources/styles/mixins";

    button {
        cursor: pointer;
        @include hover-transition;
    }

    a {
        display: block;
        text-decoration: none;
        outline: none;
        color: inherit;
        width: 100%;
    }

    .normal {
        border-radius: 20px;
        font-size: 16px;
        color: $text-color;
        background-color: $button-bg-color;
        margin-right: 20px;
        font-weight: 500;

        &.primary {
            color: #ffffff;
            background-color: $button-bg-color2;
        }

        a {
            padding: 10px 24px;
        }

        &:last-child {
            margin-right: 0;
        }

        &:hover {
            color: #ffffff;
            background-color: $button-hover-color;
        }
    }

    .full {
        text-transform: uppercase;
        border-radius: 6px;
        background-color: $button-bg-color2;
        width: 100%;
        color: #ffffff;
        font-weight: 600;

        &.primary {
            color: $button-bg-color2;
            background-color: transparent;
            border: 2px solid $button-bg-color2;
        }

        &:hover {
            color: #ffffff;
            background-color: $background-color;
            border-color: $background-color;
        }

        @include responsive(large) {
            font-size: 18px;
            line-height: 24px;
            letter-spacing: 2px;

            a { padding: 24px 0; }
        }
        @include responsive(medium) {
            font-size: 12px;
            line-height: 16px;
            letter-spacing: 1.4px;

            a { padding: 15px 0; }
        }

        @include responsive(small) {
            font-size: 15px;
            line-height: 16px;
            letter-spacing: 1.8px;

            a { padding: 12px 0; }
        }
    }
</style>
