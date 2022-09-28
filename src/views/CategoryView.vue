<script setup lang="ts">
import { provide } from "vue";
import { BookItem } from "@/types";
import CategoryNav from "@/components/CategoryNav.vue";
import CategoryBookList from "@/components/CategoryBookList.vue";
const bookList: BookItem[] = [
  {
    bookId: 1001,
    title: "Every Summer",
    author: "Homer",
    price: 699,
    isPublic: true,
    readNow: false,
  },
  {
    bookId: 1002,
    title: "Craw Dads",
    author: "Fyodor Dostoyevski",
    price: 1399,
    isPublic: false,
    readNow: true,
  },
  {
    bookId: 1003,
    title: "Woman Fire",
    author: "Charles Dickens",
    price: 599,
    isPublic: true,
    readNow: false,
  },
  {
    bookId: 1004,
    title: "The Office",
    author: "Herman Melville",
    price: 699,
    isPublic: true,
    readNow: true,
  },
];
// provide("bookList", bookList);
</script>

<style scoped>
.category-page {
  display: flex;
  flex-direction: row;
}
</style>

<template>
  <div class="category-page">
    <category-nav></category-nav>
    <category-book-list :bookList="bookList"> </category-book-list>
  </div>
</template>
