<style lang="scss" scoped>
.site-header{
    background-color: $black-dark;
    height: $header-height-mobile;
    display: flex;
    padding: 10px 30px;

    @include desktop{
        height: $header-height;
        padding: 0;
    }


    .mobile-menu-icon{
        color: $blue-light;
        font-size: 24px;
        cursor: pointer;
        padding-right: 25px;
    }

    &__logo{
        &__img{
            width: 185px;
        }
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
        <div class="max-content-width full">
            <div class="columns is-vcentered is-gapless is-flex-touch">
                <div class="column is-hidden-desktop is-one-fifth-mobile is-1-tablet">
                    <i @click="mobileMenuOpen = true" class="fa fa-bars mobile-menu-icon" aria-hidden="true"></i>
                </div>
                <div class="column is-two-fifths-desktop site-header__logo">
                    <img class="site-header__logo__img" src="../../assets/images/logo.svg" alt="logo">
                </div>
                <div class="column is-hidden-touch">
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

        <mobile-menu @close="mobileMenuOpen = false" :open="mobileMenuOpen"></mobile-menu>

    </header>
</template>

<script>
    import MobileMenu from './mobile-menu';
    export default {
        components: { MobileMenu },
        props:[''],
        data: function(){
            return{
                mobileMenuOpen: false
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
