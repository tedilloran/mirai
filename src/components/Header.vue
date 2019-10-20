<template>
    <section class="section header">
        <div class="inner">
            <div class="inner__content">
                <div class="inner__content--main">
                    <h1 class="title">consequat semper viverra nam libero</h1>
                    <h2 class="title--sub">consequat semper viverra nam libero</h2>
                </div>
                <div class="inner__content--sub">
                    <img class='lightbulb' ref='lightbulb' src="@/assets/light_off.svg">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { TimelineMax, Elastic } from 'gsap/TweenMax';

export default {
    name: 'Header',
    mounted() {
        const { lightbulb } = this.$refs;
        const tl = new TimelineMax({ repeat: -1, yoyo: true });
        tl.to(lightbulb, 1, {rotationZ: 180 });
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
            border: 0.1rem solid $color-primary;
            border-radius: 0.3rem;

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

                .lightbulb {
                    transform: rotate(180deg);
                    position: relative;
                }
            }
        }
    }
}
</style>