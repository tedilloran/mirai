<template>
  <div id="app">
    <Header/>
    <Nav/>
    <Content>
      Testasdasdasd
    </Content>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import BackgroundVideo from "./components/BackgroundVideo.vue";
import Content from "./components/Content.vue";
import Nav from "./components/Nav";

export default {
  name: "app",
  components: {
    Header,
    Nav,
    Content,
    BackgroundVideo
  }
};
</script>

<style lang='scss'>
#app {
  z-index: 0;
  width: 100%;
  box-sizing: border-box;
  margin-left: 4rem;
  margin-top: 4rem;
}
</style>
