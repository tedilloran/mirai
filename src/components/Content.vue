<template>
  <section class="section content">
    <div class="content__inner">
      <form action method="get">
        <div class="form-main-row">
          <label class="label" for="query">Search</label>
          <input
            placeholder="Search for something on Spotify!"
            name="query"
            id="query"
            class="input-text"
            type="text"
          />
          <button class="button" name="search" type="submit">
            <i class="fas fa-search"></i>
          </button>
          <div class="search-type">
            <label class="search-type-option">
              <input type="radio" name="search-type" />
              <span class="search-type-option-text">All</span>
            </label>
            <label class="search-type-option">
              <input type="radio" name="search-type" />
              <span class="search-type-option-text">Artist</span>
            </label>
            <label class="search-type-option">
              <input type="radio" name="search-type" />
              <span class="search-type-option-text">Album</span>
            </label>
            <label class="search-type-option">
              <input type="radio" name="search-type" />
              <span class="search-type-option-text">Track</span>
            </label>
          </div>
        </div>
      </form>
      <table></table>
    </div>
  </section>
</template>

<script>
export default {
  name: "Content"
};
</script>

<style scoped lang="scss">
.content {
  height: 50rem;

  &__inner {
    color: $color-secondary;
    background-color: rgba($color-gray-light, 0.6);
    width: 100%;
    height: 100%;
    padding: 3rem;
    overflow-y: auto;

    .form-main-row {
      margin-bottom: 3rem;
      display: grid;
      grid-template-columns: min-content 1fr min-content;
      grid-template-rows: 1fr 1fr;
      grid-column-gap: 1rem;
      align-items: center;

      .search-type {
        grid-column-start: 2;
        align-self: center;
        display: flex;
        align-items: center;

        &-option {
          display: flex;
          align-items: center;
          &:not(:last-of-type) {
            margin-right: 1rem;
          }

          input[type="radio"] {
            margin-right: 0.5rem;
          }

          &-text {
            text-align: start;
          }
        }
      }

      .label {
        display: flex;
        align-items: center;
      }

      & > * {
        height: 100%;
      }
    }
  }
}
</style>