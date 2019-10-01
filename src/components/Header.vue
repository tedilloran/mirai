<template>
    <div class="header">
    </div>
</template>

<script>
var Header = {
    name: 'Header',

};
export default Header;
</script>

<style scoped lang="scss">
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 50rem;
    background-color: rgba($color-black, 0.7);
    z-index: 1;
}
</style>