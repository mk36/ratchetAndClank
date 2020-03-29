<style lang="scss" scoped>
.release-section{
    @include setBackgroundImage('~../../assets/images/banner/bannerImages.jpg');
    background-position: top;

    h2{
        color: $white;
    }

    img{
        @include paddingBorderBox(0 25px);

        @include desktop{
            @include paddingBorderBox(0);
        }
    }
}
</style>

<template>
    <section class="release-section section-padding">
        <div class="max-content-width">
            <section class="release-section__content columns">
                <img :src="getImgUrl('images/release/available.png')" alt="" class="column">
                <img :src="getImgUrl('images/release/platforms.png')" alt="" class="column">
                <img :src="getImgUrl('images/release/publisher.png')" alt="" class="column">
                <img :src="getImgUrl('images/release/rating.png')" alt="" class="column">
           </section>
        </div>

    </section>
</template>

<script>

    export default {
        components: {

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

            },
            getImgUrl(url) {
                return require('../../assets/'+ url);
            }
        }
    }
</script>
