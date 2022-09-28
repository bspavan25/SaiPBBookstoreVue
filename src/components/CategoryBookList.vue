<script setup lang="ts">
import { defineProps } from "vue"; // needed if you don't want an error below
import { BookItem } from "@/types";
import CategoryBookListItem from "@/components/CategoryBookListItem.vue";
const props = defineProps<{
  bookList: BookItem[];
}>();
</script>

<style scoped>
.book-boxes {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding: 0.5em;
  gap: 0.5em;
}
.category-main-frame {
  display: flex;
  flex-direction: column;
  align-content: center;
  padding: 0.5em;
  border: 1px solid black;
  width: 60em;
  height: 34em;
}

.category-sort-bar {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0.8em;
  margin: 0.5em;
}

.books-change-order {
  display: flex;
  font-size: 30px;
  gap: 0.4em;
  color: var(--primary-color-dark);
}

.sort-button {
  padding: 0.75em 0.75em;
  font-weight: lighter;
  font-family: var(--title-font-family);
  font-size: 15px;
  border-radius: 10px;
  border: 2.5px solid var(--primary-color-dark);
}
</style>

<template>
  <section class="category-main-frame">
    <section class="category-sort-bar">
      <div class="books-change-order">
        <i class="fa-solid fa-grip"></i>
        <i class="fa-solid fa-table-cells-large"></i>
      </div>
      <div>
        <button class="sort-button button">
          Sort by : Relevance
          <i class="fa-solid fa-caret-down"></i>
        </button>
      </div>
    </section>
    <section class="category-book-list">
      <ul class="book-boxes">
        <template v-for="book in bookList" :key="book.bookId">
          <category-book-list-item :book="book"></category-book-list-item>
        </template>
      </ul>
    </section>
  </section>
</template>
