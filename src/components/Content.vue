<template>
<section class="section content">
    <div class="content__inner">
        <form>
            <div class="form-main-row">
                <label class="label" for="query">Search</label>
                <input id="query" class="input-text" type="text">
                <button class="button">
                    <i class="fas fa-search"></i>
                </button>
            </div>
        </form>
    </div>
</section>
</template>

<script>
export default {
    name: 'Content'
};
</script>

<style scoped lang="scss">
.content {
    height: 50rem;

    &__inner {
        color: $color-secondary;
        background-color: rgba($color-white, 0.6);
        width: 100%;
        height: 100%;
        padding: 3rem;
    }
}
</style>