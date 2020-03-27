<style lang="scss" scoped>
    .sub-nav{
        text-align: center;
        background-color: $black-light;

        &.sticky{
            width: 100%;
            @include positioningOffset(fixed, $header-height, unset, unset, 0);
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
    <div class="sub-nav">
        <p href="#" @click="scrollToSection('.image-section')">Images</p>
        <p href="#"  @click="scrollToSection('.overview-section')">Overview</p>
        <p href="#"  @click="scrollToSection('.video-section')">Videos</p>
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
                let nav = document.querySelector('.sub-nav');
                let subNavTop = nav.offsetTop - (nav.offsetHeight * 2);

                document.addEventListener('scroll', function () {
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
