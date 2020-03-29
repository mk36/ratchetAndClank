<style lang="scss" scoped>
.mobile-menu{
    @include positioningOffset(fixed, 0, unset, unset, 0);
    z-index: $z-index-modal;
    width: 100%;
    height: 100vh;
    transition: transform 0.3s ease-in-out;
    transform: translateX(-110%);

    &.open{
        transform: translateX(0);
    }

    &__content{
        background-color: $white;
        width: 300px;
        height: 100%;
        @include paddingBorderBox(25px);

        &__logo{
            margin-bottom: 15px;
        }

        &__nav{
            flex-direction: column;
            text-transform: uppercase;

            a{
                margin-bottom: 20px;
            }
        }
    }
}
</style>

<template>
    <div class="mobile-menu" :class="{'open': open}" @click="closeMenu($event)">
        <section class="mobile-menu__content">
            <div class="mobile-menu__content__logo">
                <img class="site-header__logo__img" src="../../assets/images/logoDark.svg" alt="logo">
            </div>

            <nav class="mobile-menu__content__nav is-flex">
                <a href="">Home</a>
                <a href="">Games</a>
                <a href="">Careers</a>
                <a href="">News</a>
                <a href="">Community</a>
                <a href="">Support</a>
                <a href="">Store</a>
            </nav>
        </section>
    </div>
</template>

<script>
    export default {
        components: {},
        props:['open'],
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
            closeMenu(event){
                let vm = this;
                if(event.originalTarget.classList.contains('open')){
                    vm.$emit('close', true);
                }
            }
        }
    }
</script>
