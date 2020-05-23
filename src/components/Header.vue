<template>
    <header class="header">
        <div class="header__content">
            <div class="input-button">
                <input placeholder="Search..." class="input-text" type="text" name="search" />
                <button class="button">
                    <i class="fas fa-search"></i>
                </button>
            </div>
        </div>
    </header>
</template>

<script>

export default {
    name: 'Header'
};
</script>

<style scoped lang="scss">
    .header {
        position: fixed;
        top: 0;
        right: 0;
        width: calc(100% - #{$nav-width});
        height: $header-height;
        background-color: rgba($color-gray-dark, 0.8);

        &__content {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
            width: 100%;
            padding: 1rem;
        }
    }
</style>