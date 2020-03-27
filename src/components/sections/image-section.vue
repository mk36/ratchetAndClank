<style lang="scss" scoped>
.image-section{
    @include setBackgroundImage('~../../assets/images/banner/bannerImages.jpg');

    h2{
        color: $white;
    }
}
</style>

<template>
    <section class="image-section section-padding">
        <div class="max-content-width">
            <h2>IMAGES</h2>
            <hr class="title-divider">

            <section class="image-section__images zoom-image columns">
                <zoom-image class="column" url="images/promo/nexus1.jpg"></zoom-image>
                <zoom-image class="column" url="images/promo/acit1.jpg"></zoom-image>
                <zoom-image class="column" url="images/promo/tools.jpg"></zoom-image>
           </section>
        </div>

    </section>
</template>

<script>
    import ZoomImage from '../zoom-image/zoom-image.vue';
    export default {
        components: {
            ZoomImage
        },
        props:[''],
        data: function(){
            return{
                test: ''
            }
        },
        mounted: function () {
            this.setUp();
        },
        methods: {
            setUp: function () {

            }
        }
    }
</script>
