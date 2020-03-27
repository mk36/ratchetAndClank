<style lang="scss" scoped>
    .video-section{
        @include setBackgroundImage('~../../assets/images/banner/bannerImages.jpg');

        h2{
            color: $white;
        }

        &__videos{
            &__video{
                iframe{
                    width: 100%;
                    height: 260px;
                }

                color: $white;

                &__title{
                    font-weight: 600;
                }
            }
        }
    }
</style>

<template>
    <section class="video-section section-padding">
        <div class="max-content-width">
            <h2>Videos</h2>
            <hr class="title-divider">

            <section class="video-section__videos columns">
                <div class="video-section__videos__video column">
                    <iframe src="https://www.youtube-nocookie.com/embed/W0qU15NOj2k?rel=0&showinfo=0"></iframe>
                    <p class="video-section__videos__video__title">
                        Ratchet & Clank: Into the Nexus
                    </p>
                    <p>
                        PlayStation 3 - 2013
                    </p>
                </div>
                <div class="video-section__videos__video column">
                    <iframe src="https://www.youtube-nocookie.com/embed/nhv1cLlskeQ?rel=0&showinfo=0"></iframe>
                    <p class="video-section__videos__video__title">
                        Ratchet & Clank: Full Frontal Assault
                    </p>
                    <p>
                        PlayStation 3 - 2012
                    </p>
                </div>
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

            }
        }
    }
</script>
