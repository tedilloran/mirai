<template>
    <section class="section header">
        <div class="inner">
            <div class="inner__content">
                <div class="inner__content--main">
                    <h1 class="title">consequat semper viverra nam libero</h1>
                    <h2 class="title--sub">consequat semper viverra nam libero</h2>
                </div>
                <div class="inner__content--sub">
                    <img class='main-img' ref='mainImage' src="@/assets/vinyl.svg">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { TimelineMax, Power0 } from 'gsap/TweenMax';

export default {
    name: 'Header',
    mounted() {
        const { mainImage } = this.$refs;
        const tl = new TimelineMax({ repeat: -1});
        tl.to(mainImage, 2, { ease: Power0.easeNone, rotationZ: 360 })
            .smoothChildTiming(true);
    }
};
</script>

<style scoped lang="scss">
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 50rem;
    z-index: 2;

    .inner {
        z-index: 2;
        width: 100%;
        height: 100%;
        padding: 3rem;
        border-radius: 0.3rem;
        background-color: rgba($color-gray, 0.2);

        &__content {
            display: grid;
            grid-template-columns: 3fr 2fr;
            grid-template-rows: 1fr;
            grid-column-gap: 1rem;
            width: 100%;
            height: 100%;
            border: 1px solid $color-primary;

            &--main {
                padding: 3rem;
                display: flex;
                flex-direction: column;
                justify-content: center;

                .title {
                    color: $color-white;
                    text-transform: capitalize;

                    &--sub {
                        color: $color-secondary;
                        text-transform: uppercase;
                        letter-spacing: 1.6rem;
                    }
                }
            }

            &--sub {
                display: flex;
                justify-content: center;
                align-items: center;
                overflow: hidden;

                .main-img {
                    height: 100%;
                    width: 100%;
                    position: relative;
                }
            }
        }
    }
}
</style>