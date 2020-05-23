<template>
  <nav class="nav">
    <div class="nav__content">
      <a class="nav__item" title="Home">
        <i class="fas fa-home"></i>
      </a>
      <a class="nav__item" title="Search">
        <i class="fas fa-search"></i>
      </a>
      <a class="nav__item" title="Charts">
        <i class="fas fa-chart-bar"></i>
      </a>
    </div>
    <div class="nav__sub">
      <a class="nav__item" title="Spotify Player">
        <i class="far fa-dizzy"></i>
      </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Nav"
};
</script>

<style scoped lang="scss">
.nav {
  align-items: center;
  background-color: rgba($color-gray-dark, 0.8);
  display: flex;
  flex-direction: column;
  height: 100vh;
  justify-content: space-between;
  left: 0;
  position: fixed;
  top: 0;
  width: $nav-width;

  &__content {
    align-items: center;
    color: $color-white;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: repeat(5, $nav-width);
    justify-items: center;
    width: 100%;
  }

  &__sub {
    height: 4rem;
    width: 4rem;
  }

  &__item {
    align-items: center;
    border-bottom: 1px solid rgba($color-white, 0.1);
    color: #ffffff;
    display: flex;
    height: 100%;
    justify-content: center;
    transition: background-color 0.2s;
    width: 100%;

    &:hover {
      background-color: rgba($color-white, 0.1);
    }
  }

}
</style>