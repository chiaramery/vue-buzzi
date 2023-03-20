<script>
export default {
    name: 'AboutUs',
    data() {
        return {
            activeSlide: 0,
            autoplay: null,
            slides: [
                {
                    image: "src/img/7.JPG",
                },
                {
                    image: "src/img/25.JPG",
                },
                {
                    image: "src/img/2.JPG",
                },
            ],
        }
    },
    created() {
        this.startAutoplay();
    },
    methods: {
        showNext() {
            if (this.activeSlide < this.slides.length - 1) {
                this.activeSlide++;
            } else {
                this.activeSlide = 0;
            }
        },
        showPrev() {
            if (this.activeSlide > 0) {
                this.activeSlide--;
            } else {
                this.activeSlide = this.slides.length - 1;
            }
        },
        showItem(itemIndex) {
            this.activeSlide = itemIndex;
        },
        stopAutoplay() {
            console.log("stop");
            clearInterval(this.autoplay);
            this.autoplay = null;
        },
        startAutoplay() {
            if (this.autoplay === null) {
                this.autoplay = setInterval(() => {
                    console.log("interval");
                    this.showNext();
                }, 5000);
            }
        },
    },
}
</script>

<template>
    <div id="servizi">
        <div class="row justify-content-around">
            <div class="col-4">
                <div class="text-servizi">
                    <h3 class="text-center pt-1">I nostri servizi:</h3>
                    <div class="list">
                        <ul>
                            <li>perforazione e trivellazione pozzi artesiani</li>
                            <li>ripristino pozzi già esistenti</li>
                            <li>installazione e manutenzione pompe sommerse</li>
                            <li>installazione e manutenzione autoclavi</li>
                            <li>punte abbissine</li>
                            <li>scavi per piccoli spazi</li>
                            <li>movimento terra</li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="col-4">
                <div class="slider-wrapper" tabindex="0" @focus="stopAutoplay" @blur="startAutoplay" @keyup.up="showPrev"
                    @keyup.down="showNext">
                    <div class="item">
                        <img :src="slides[activeSlide].image" :alt="slides[activeSlide].title" />
                        <div class="text">
                            <h5 class="text-center">{{ slides[activeSlide].title }}</h5>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<style lang="scss">
#servizi {
    position: relative;
    width: 100%;

    .back {
        width: 100%;
        height: 100vh;

        .text-b {
            width: 45%;
            margin: 1em auto;
            background-color: rgb(11 113 184);
        }
    }

    .col-4 {
        .text-servizi {
            margin-top: 2em;
            background-color: rgb(11 113 184);
            color: white;

            h3 {
                font-size: 2em;
            }

            .list {
                padding-left: 8em;

                li {
                    padding-top: .5em;
                    padding-bottom: .5em;
                    font-size: 1.5em;
                }
            }
        }
    }

    .col-4 {
        .slider-wrapper {
            padding-top: .5em;
        }
    }
}
</style>