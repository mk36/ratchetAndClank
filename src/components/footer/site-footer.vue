<style lang="scss" scoped>
    .site-footer{
        text-align: center;

        @include desktop{
            text-align: left;
        }

        &__links{
            background-color: $black-light;

            &__list{
                color: $blue-light;
                &__title{
                    font-weight: 600;
                    margin-bottom: 10px;
                }

                li{
                    line-height: 2;
                }
            }
        }

        &__address{
            background-color: $black-dark;

            .footer-logo{
                max-width: 160px;
            }

            &__option{
                color: $white;

                li:first-child{
                    font-weight: 600;
                }
            }
        }
    }
</style>

<template>
    <footer class="site-footer">
        <section class="site-footer__links section-padding">
            <div class="max-content-width">
                <div class="columns">
                    <ul class="column site-footer__links__list">
                        <li class="site-footer__links__list__title">Games</li>
                        <li>Marvel’s Spider-Man</li>
                        <li>Stormland </li>
                        <li>The Unspoken </li>
                        <li>Ratchet & Clank (PS4) </li>
                        <li>Edge of Nowhere </li>
                        <li>Sunset Overdrive </li>
                    </ul>

                    <ul class="column site-footer__links__list">
                        <li class="site-footer__links__list__title">Careers</li>
                        <li>Working At Insomniac </li>
                        <li>Job Openings</li>
                        <li>Moonlighting</li>
                        <li>Baker’s Dozen</li>
                        <li>Career Inquiries</li>
                    </ul>

                    <ul class="column site-footer__links__list">
                        <li class="site-footer__links__list__title">Community</li>
                         <li>Press & Media</li>
                         <li>Discord</li>
                         <li>Twitter</li>
                         <li>Facebook</li>
                         <li>Instagram</li>
                         <li>Reddit</li>
                         <li>YouTube</li>
                         <li>Twitch</li>
                    </ul>

                    <ul class="column site-footer__links__list">
                        <li class="site-footer__links__list__title">Contact Us</li>
                        <li>Game Support</li>
                        <li> Terms Of Use</li>
                        <li> Privacy Policy</li>
                        <li>California Privacy Rights</li>
                    </ul>
                </div>
            </div>
        </section>

        <section class="site-footer__address section-padding">
            <div class="max-content-width">
                <div class="columns is-vcentered">
                    <section class="column">
                        <img class="footer-logo" src="../../assets/images/logo.svg" alt="logo">
                    </section>

                    <ul class="site-footer__address__option column">
                        <li>Burbank Studio</li>
                        <li>2255 N Ontario St.</li>
                        <li>Suite 550</li>
                        <li>Burbank, CA 91504</li>
                    </ul>

                    <ul class="site-footer__address__option column">
                        <li>Durham Studio</li>
                        <li>7806 NC Highway 751</li>
                        <li>Suite 300</li>
                        <li>Durham, NC 27713</li>
                    </ul>
                </div>
            </div>
        </section>

    </footer>
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
