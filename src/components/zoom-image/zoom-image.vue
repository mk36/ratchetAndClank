<style lang="scss" scoped>
.zoom-image{
    &__placeholder{
        cursor: zoom-in;
        transition: opacity 0.5s ease;

        &:hover{
            opacity: 0.8;
        }
     }

    &__modal{
        display: none;
        @include positioningOffset(fixed, 0, unset, unset, 0);
        z-index: 10;
        background-color: $black-mid;
        width: 100%;
        height: 100%;


        &.show{
            display: block;
        }

        &__image{
            @include centerContent();
            cursor: zoom-out;
            @include paddingBorderBox(50px);
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}
</style>

<template>
    <div class="zoom-image">
        <img @click="show = true" class="zoom-image__placeholder" :src="getImgUrl(url)" alt="">

        <div class="zoom-image__modal" :class="{'show': show}" @click="show = false">
            <img  class="zoom-image__modal__image" :src="getImgUrl(url)" alt="">
        </div>

    </div>
</template>

<script>
    export default {
        components: {},
        props:['url'],
        data: function(){
            return{
                show: false
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
