<script setup lang="ts">
import { inject } from "vue";
const categoryList = inject("categoryList");
</script>

<style scoped>
.header-dropdown {
  position: relative;
}

.categories-button {
  background-color: var(--primary-color-dark);
  color: var(--primary-background-color);
  height: 40px;
}

.header-dropdown ul {
  background-color: var(--secondary-background-color);
  color: black;
  display: none;
  border: 1px solid black;
  border-radius: 6px;
  width: 145px;
}

.header-dropdown li {
  padding: 0.25em 0.5em;
}

.header-dropdown a {
  color: black;
  text-decoration: none;
}

.header-dropdown li:hover {
  background: lightgray;
  text-decoration: underline;
}

.header-dropdown:hover ul {
  display: block;
  position: absolute;
  min-width: 8em;
  z-index: 1;
  cursor: pointer;
}
</style>

<template>
  <section class="header-dropdown">
    <div>
      <button class="button categories-button">
        CATEGORIES
        <i class="fa-solid fa-caret-down"></i>
      </button>
      <ul>
        <li v-for="category in categoryList" :key="category.categoryId">
          <router-link :to="'../category/' + category.name">
            {{ category.name }}
          </router-link>
        </li>
      </ul>
    </div>
  </section>
</template>
