<template>
  <div id="app">
    <Header></Header>
    <BackgroundVideo></BackgroundVideo>
    <Content></Content>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import BackgroundVideo from "./components/BackgroundVideo.vue";
import Content from "./components/Content.vue";
import Footer from "./components/Footer";

export default {
  name: "app",
  components: {
    Header,
    BackgroundVideo,
    Content,
    Footer
  }
};
</script>

<style lang='scss'>
#app {
  z-index: 0;
  width: 100%;
  box-sizing: border-box;
  padding: 3rem;
}
</style>
