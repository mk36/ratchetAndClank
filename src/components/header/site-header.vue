<style lang="scss" scoped>
.site-header{
    background-color: $black-dark;
    height: $header-height;
    display: flex;

    &__logo{
        width: 185px;
    }

    &__nav{
        text-align: center;
        a{
            color: $blue-light;
            text-transform: uppercase;
            font-size: .85rem;

            &:hover{
                color: $white;
            }

            &:not(:last-child){
                @include paddingBorderBox(0 40px 0 0);
            }
        }
    }
}
</style>

<template>
    <header class="site-header navbar is-fixed-top">
        <div class="max-content-width">
            <div class="columns is-vcentered is-gapless">
                <div class="column is-two-fifths"><img class="site-header__logo" src="../../assets/images/logo.svg" alt="logo"></div>
                <div class="column">
                    <nav class="site-header__nav">
                        <a href="">Games</a>
                        <a href="">Careers</a>
                        <a href="">News</a>
                        <a href="">Community</a>
                        <a href="">Support</a>
                        <a href="">Store</a>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        components: {},
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
