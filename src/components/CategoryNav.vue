<script setup lang="ts">
import { inject } from "vue";
const categoryList = inject("categoryList");
</script>

<style scoped>
.categories-text-logo {
  font-family: var(--title-font-family);
  font-size: 140%;
  color: white;
  padding: 10%;
}

.category-side-bar {
  display: flex;
  flex-direction: column;
  /*align-items: center;*/
  padding: 0.5em;
  background-color: var(--primary-color);
  width: 30%;
  font-size: 19px;
  font-family: var(--title-font-family);
  border: 1px solid black;
  min-width: 10em;
}

.category-buttons {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 0.65em;
}

.category-side-bar-button,
.category-side-bar-button:visited {
  display: inline-block;
  background: var(--primary-color);
  color: var(--primary-background-color);
  text-decoration: none;
  padding: 0.5em 1em;
  cursor: pointer;
  border-radius: 7px;
  width: 100%;
}

.category-side-bar-button:hover,
.category-side-bar-button:active {
  background: var(--primary-color);
  color: var(--primary-background-color);
}

.category-side-bar-button.selected-category-button {
  background-color: var(--card-background-color);
  color: var(--primary-color);
  text-decoration: underline;
}

.category-side-bar-button.unselected-category-button,
.category-side-bar-button.unselected-category-button:visited {
  background-color: var(--primary-color);
}

.category-side-bar-button.unselected-category-button:hover,
.category-side-bar-button.unselected-category-button:active {
  background-color: var(--primary-background-color);
  color: var(--primary-color);
}
</style>

<template>
  <section class="category-side-bar">
    <div class="categories-text-logo">CATEGORIES:</div>
    <ul class="category-buttons">
      <li v-for="category in categoryList" :key="category.categoryId">
        <router-link
          :to="'../category/' + category.name"
          class="category-side-bar-button"
          :class="
            category.name == 'Scify'
              ? 'selected-category-button'
              : 'unselected-category-button'
          "
        >
          {{ category.name }}
        </router-link>
      </li>
    </ul>
  </section>
</template>
