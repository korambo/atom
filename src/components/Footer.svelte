<script>
    import cn from 'classnames';

    import Button from './Button.svelte';
    import Row from './Row.svelte';

    import Logo from './../_sources/icons/logo.svg';
    import SocialBe from './../_sources/icons/social_be.svg';
    import SocialDr from './../_sources/icons/social_dr.svg';
    import SocialIn from './../_sources/icons/social_in.svg';
    import SocialFb from './../_sources/icons/social_fb.svg';

    const links = [
        {
            title: 'Products',
            type: 'text',
            items: [
                { title: 'UI Kit & Design System' },
                { title: 'Illustrations' },
            ]
        }, {
            title: 'About',
            type: 'text',
            items: [
                { title: 'License', url: 'https://the18.design/license' },
                { title: 'Contact Us', url: 'mailto:the18.design@gmail.com' },
            ]
        }, {
            title: 'Socials',
            type: 'button',
            items: [
                { img: SocialBe, url: 'https://www.behance.net/The18design' },
                { img: SocialDr, url: 'https://dribbble.com/18Design_Co' },
                { img: SocialIn, url: 'https://www.instagram.com/the18.design' },
                { img: SocialFb, url: 'https://www.facebook.com/the18.design' },
            ]
        },
    ];
</script>

<footer>
    <Row>
        <div class="price">
            <div class="price_item">
                <img src="/images/footer_buy1.svg" alt="free_demo">
                <div class="price_button">
                    <Button text="try it free" type="full" primary url="https://gumroad.com/l/OcePo" />
                </div>
            </div>
            <div class="price_item">
                <img src="/images/footer_buy2.svg" alt="full_version">
                <div class="price_button">
                    <Button text="BUY FULL FOR $49" type="full" />
                </div>
            </div>
        </div>

        <div class="sub_footer">
            <div class="logo">
                <a class="logo_title" href="http://the18.design">
                    <div class="logo_icon">{@html Logo}</div>
                    <span>18 Design</span>
                </a>
                <p class="logo_desc">
                    Collection of elements that will make
                    your workflow faster and more productive.
                </p>
            </div>

            {#each links as linkBlock}
                <div class="links_list">
                    <div class="links_list_title">{linkBlock.title}</div>
                    <ul class={cn({ links_list_column: linkBlock.type === 'text' })}>
                        {#each linkBlock.items as link}
                            <li>
                                <a class={cn({ disabled: !link.url })} href={link.url} target="_blank">
                                    {#if linkBlock.type === 'text'}
                                        {link.title}
                                    {:else}
                                        <div class="links_list_img">{@html link.img}</div>
                                    {/if}
                                </a>
                            </li>
                        {/each}
                    </ul>
                </div>
            {/each}
        </div>
    </Row>
</footer>

<style lang="scss">
    @import "../_sources/styles/variables";
    @import "../_sources/styles/mixins";

    footer {
        @include responsive(large) {
            padding: 100px 0;
        }
        @include responsive(medium) {
            padding: 54px 0 60px;
        }
        @include responsive(small) {
            padding: 60px 0;
        }
    }

    .price {
        display: flex;
        justify-content: center;

        &_item {
            width: 100%;
            position: relative;

            @include responsive(large) {
                margin-right: 40px;
            }
            @include responsive(medium) {
                margin-right: 26px;
            }

            @include responsive(small) {
                margin-bottom: 20px;
            }

            &:last-child {
                margin: 0;
            }
        }

        &_button {
            position: absolute;

            @include responsive(large) {
                left: 28px;
                bottom: 32px;
                width: calc(100% - 56px);
            }
            @include responsive(medium) {
                left: 20px;
                bottom: 20px;
                width: calc(100% - 40px);
            }

            @include responsive(small) {
                left: 18px;
                bottom: 19px;
                width: calc(100% - 36px);
            }
        }

        @include responsive(small) {
            flex-direction: column;
            align-items: center;
        }
    }

    .sub_footer {
        display: grid;

        @include responsive(large) {
            padding-top: 120px;
            grid-template-columns: 390px repeat(3, 1fr);
            grid-column-gap: 10px;
        }
        @include responsive(medium) {
            padding-top: 60px;
            grid-template-columns: repeat(3, 1fr);
            grid-row-gap: 40px;
        }
        @include responsive(small) {
            padding-top: 60px;
            grid-template-columns: 1fr;
            grid-row-gap: 40px;
        }
    }

    .logo {
        @include responsive(medium) {
            grid-column: 1 / 4;
            margin: auto;
            text-align: center;
        }

        @include responsive(small) {
            margin: auto;
            text-align: center;
        }

        &_icon {
            width: 40px;
            margin-right: 10px;
        }

        &_title {
            display: flex;
            color: $text-color2;
            font-size: 20px;
            font-weight: 500;
            letter-spacing: 1px;

            span {
                line-height: 40px;
            }

            @include responsive(medium) {
                justify-content: center;
            }

            @include responsive(small) {
                justify-content: center;
            }
        }

        &_desc {
            font-size: 17px;
            margin-top: 10px;;
            color: $text-color4;
            max-width: 332px;
            line-height: 28px;
        }
    }

    .links_list {
        @include responsive(large) {
            &:nth-child(3) {
                padding-left: 38px;
            }
        }

        @include responsive(medium) {
            &:nth-child(3) {
                justify-self: center;
            }
            &:nth-child(4) {
                justify-self: self-end;
            }
        }

        @include responsive(small) {
            text-align: center;
        }

        &_column {
            flex-direction: column;
        }

        &_title {
            font-size: 24px;
            line-height: 28px;
            font-weight: 700;
            color: $text-color2;
        }

        ul {
            display: flex;
            margin-top: 16px;

            @include responsive(small) {
                justify-content: center;
            }
        }

        li {
            margin-bottom: 6px;
            line-height: 28px;

            &:last-child {
                margin-bottom: 0;
            }
        }

        a {
            color: $text-color4;
            font-size: 17px;
            @include hover-transition;

            &:hover {
                color: $text-color2;
            }
        }

        a.disabled {
          opacity: .4;
          cursor: default;

          &:hover {
            color: $text-color4;
          }
        }

        &_img {
            width: 44px;
            margin-right: 10px;
            opacity: .5;
            @include hover-transition;

            &:last-child {
                margin-bottom: 0;
            }

            &:hover {
                opacity: 1;
            }
        }
    }
</style>