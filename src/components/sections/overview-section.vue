<style lang="scss" scoped>
    .overview-section{
        background-color: $white;

        &__text, &__list{
            color: $black-text;

            p{
                margin-bottom: 15px;
            }
        }

        &__list{
            list-style: outside circle;
            margin-left: 25px;
        }

        h2, h4{
            color: $black-dark;
        }

        .title-divider{
            background-color: $grey-dark;
        }
    }
</style>

<template>
    <section class="overview-section section-padding">
        <div class="max-content-width">
            <div class="columns">
                <section class="column">
                    <h2>OVERVIEW</h2>
                    <hr class="title-divider">

                    <div class="overview-section__text">
                        <p>
                            In 2002, Insomniac Games might not have imagined that Ratchet & Clank would have spawned nearly a dozen games and a movie. Yet Ratchet & Clank has charmed PlayStation fans for 15 years and hit all sorts of milestones. Its first four PlayStation 2 games all earned “Greatest Hits” status. Ratchet & Clank was the first Western-developed game to be bundled with a game console in Japan.
                        </p>

                        <p>
                            The duo’s 11 PlayStation console games have run the gamut from single-player adventures, to online competitive multiplayer, to four-player fun for the entire family. In 2016, a major motion picture hit theatres around the world, bringing Ratchet & Clank to the big screen for the first time. The duo has starred in spin-off games, had their own comic book series, action figures, and much more.
                        </p>
                    </div>
                </section>
                <section class="column">
                    <h4>RELEASES</h4>
                    <hr class="title-divider">

                    <ul class="overview-section__list">
                        <li>Ratchet & Clank (2002) – PlayStation 2 </li>
                        <li>Ratchet & Clank: Going Commando (2003) – PlayStation 2 </li>
                        <li>Ratchet & Clank: Up Your Arsenal (2004) – PlayStation 2 </li>
                        <li>Ratchet: Deadlocked (2005) – PlayStation 2 </li>
                        <li>Ratchet & Clank Future: Tools of Destruction (2007) – PlayStation 3 </li>
                        <li>Ratchet & Clank Future: Quest for Booty (2008) – PlayStation 3 </li>
                        <li>Ratchet & Clank Future: A Crack in Time (2009) – PlayStation 3 </li>
                        <li>Ratchet & Clank: All 4 One (2011) – PlayStation 3 </li>
                        <li>Ratchet & Clank: Full Frontal Assault (2012) – PlayStation 3 </li>
                        <li>Ratchet & Clank: Into the Nexus (2013) – PlayStation 3 </li>
                        <li>Ratchet & Clank (2016) – PlayStation 4 </li>
                    </ul>
                </section>
            </div>
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
