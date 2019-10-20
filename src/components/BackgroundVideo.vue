<template>
<div class="bg-video">
    <video class="bg-video__content" muted loop autoplay>
        <source src="@/assets/background.webm" type='video/webm'/>
        <source src="@/assets/background.mp4" type='video/mp4'/>
    </video>
</div>
</template>

<script>
export default {
    name: 'BackgroundVideo'
};
</script>

<style scoped lang='scss'>
.bg-video {
    height: 100vh;
    left: 0;
    overflow: hidden;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: -1;

    &__content {
        height: auto;
        width: auto;
        object-fit: cover;
    }
}
</style>