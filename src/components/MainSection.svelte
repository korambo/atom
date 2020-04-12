<script>
    import Row from './Row.svelte';
    import ProjectName from './../_sources/icons/text-logo.svg'
</script>

<section>
    <div class="content" data-aos="fade-left">
        <div class="project_name">
            {@html ProjectName}
        </div>
        <h3 class="label">Wireframe for Sketch & Figma</h3>
        <p class="description">Tool for effective and structured design project</p>

        <div class="build_with">
            <img src="/images/header-sf.png" alt="build_with">
        </div>
    </div>
</section>

<style lang="scss">
    @import '../_sources/styles/variables.scss';
    @import '../_sources/styles/mixins.scss';

    section {
        max-width: 1400px;
        background: url("/images/header.svg") no-repeat top right;

        @include responsive(large) {
            margin:  0 auto 80px;
            padding: 140px 0 270px;
        }
        @include responsive(medium) {
            width: 773px;
            margin:  0 auto 80px;
            padding: 100px 0 115px;
        }

        @media (min-width: 493px) and (max-width: $medium - 1) {
            width: 494px;
            background-position: top right;
            margin: 0 auto 40px;
            padding: 30px 0 48px;
        }

        @media (max-width: 492px) {
            background-position: top center;
            background-size: cover;
            margin-bottom: 40px;
            padding: 30px 0 48px;
        }
    }

    .content {
        display: flex;
        flex-direction: column;
        text-align: right;
        align-items: flex-end;

        @include responsive(large) {
            padding: 0 220px;
        }
        @include responsive(medium) {
            padding: 0 120px;
        }

        @media (min-width: 493px) and (max-width: $medium - 1) {
            padding: 0 85px;
        }

        @media (max-width: 492px) {
            padding: 0 20px;
        }
    }

    .project_name {
        text-transform: uppercase;
        color: $text-color2;

        @include responsive(large) {
            font-size: 32px;
        }
        @include responsive(medium) {
            font-size: 18px;
        }
        @include responsive(small) {
            font-size: 18px;
        }
    }

    .label {
        line-height: 40px;
        color: $text-color3;
        text-transform: uppercase;
        font-weight: 600;
        letter-spacing: 1.4px;

        @include responsive(large) {
            font-size: 26px;
            margin-top: 60px;
        }
        @include responsive(medium) {
            font-size: 14px;
            margin-top: 17px;
        }
        @include responsive(small) {
            font-size: 10px;
            margin-top: 30px;
        }
    }

    .description {
        font-weight: bolder;
        text-align: right;
        color: $text-color2;
        text-transform: uppercase;

        @include responsive(large) {
            width: 728px;
            font-size: 78px;
            line-height: 94px;
            margin: 10px 0;
            letter-spacing: -2px;
        }
        @include responsive(medium) {
            width: 400px;
            font-size: 42px;
            line-height: 52px;
            margin: 6px 0 5px;
            letter-spacing: -1px;
        }
        @include responsive(small) {
            width: 240px;
            font-size: 24px;
            line-height: 32px;
            margin: 5px 0 10px;
            letter-spacing: -.5px;
        }
    }

    .build_with {
        @include responsive(large) {
            width: 126px;
        }
        @include responsive(medium) {
            width: 70px;
        }
        @include responsive(small) {
            width: 70px;
        }
    }
</style>
