<style lang="scss" scoped>
    .ratchet-site{

        .main-banner{
            width: 100%;
            height: 300px;

            @include desktop{
                height: 700px;
            }

            @include setBackgroundImage('~./assets/images/banner/bannerDesktop.jpg');
        }

        .empty-divider{
            background-color: $black-light;
            height: 50px;
        }
    }
</style>

<template>
    <div class="ratchet-site">
        <site-header></site-header>

        <section class="main-banner"></section>
        <sub-nav></sub-nav>

        <image-section></image-section>
        <overview-section></overview-section>
        <videos-section></videos-section>

        <div class="empty-divider"></div>
        <release-section></release-section>
        <site-footer></site-footer>
    </div>
</template>

<script>
    import "./styles/styles.scss";
    import SiteHeader from './components/header/site-header';
    import SubNav from './components/sub-nav/sub-nav';
    import ImageSection from './components/sections/image-section';
    import OverviewSection from './components/sections/overview-section';
    import VideosSection from './components/sections/videos-section';
    import ReleaseSection from './components/sections/release-section';
    import SiteFooter from './components/footer/site-footer';

    export default {
        name: 'App',
        components: {
            SiteHeader,
            SubNav,
            ImageSection,
            OverviewSection,
            VideosSection,
            ReleaseSection,
            SiteFooter
        }
    }
</script>
