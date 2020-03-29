<style lang="scss" scoped>
    .sub-nav-wrapper{
        height: 31px;
    }

    .sub-nav{
        text-align: center;
        background-color: $black-light;

        &.sticky{
            width: 100%;
            @include positioningOffset(fixed, $header-height-mobile, unset, unset, 0);

            @include desktop{
                @include positioningOffset(fixed, $header-height, unset, unset, 0);
            }
        }

        p{
            cursor: pointer;
            color: white;
            text-transform: uppercase;
            padding: 5px 20px;
            display: inline-block;
            font-size: .875rem;
        }
    }
</style>

<template>
    <div class="sub-nav-wrapper">
        <div class="sub-nav">
            <p href="#" @click="scrollToSection('.image-section')">Images</p>
            <p href="#"  @click="scrollToSection('.overview-section')">Overview</p>
            <p href="#"  @click="scrollToSection('.video-section')">Videos</p>
        </div>
    </div>
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
                this.snapOnScroll();
            },
            snapOnScroll(){
                document.addEventListener('scroll', function () {
                    let navWrapper = document.querySelector('.sub-nav-wrapper');
                    let nav = navWrapper.querySelector('.sub-nav');
                    let subNavTop = navWrapper.offsetTop - (navWrapper.offsetHeight * 2);
                    let pos = window.scrollY;

                    if(pos >= subNavTop){
                        nav.classList.toggle('sticky', true);
                    }
                    else{
                        nav.classList.toggle('sticky', false);
                    }
                })
            },
            /**
             * scroll to a section
             * @param id
             */
            scrollToSection(selector){
                let elm = document.querySelector(selector);

                if(elm){
                    elm.scrollIntoView({ behavior: 'smooth', block: 'center'})
                }
            }
        }
    }
</script>
