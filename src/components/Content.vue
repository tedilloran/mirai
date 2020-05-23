<template>
    <div class="content">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'Content'
};
</script>

<style scoped lang="scss">
.content {
    height: calc(100% - #{$header-height});
    width: calc(100% - #{$nav-width});
}
</style>