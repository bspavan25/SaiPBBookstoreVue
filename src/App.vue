<script setup lang="ts">
import { provide } from "vue";
import { CategoryItem } from "@/types";
import AppHeader from "@/components/AppHeader.vue";
import AppFooter from "@/components/AppFooter.vue";
const categoryList: CategoryItem[] = [
  { categoryId: 1001, name: "Scify" },
  { categoryId: 1002, name: "Fiction" },
  { categoryId: 1003, name: "Drama" },
  { categoryId: 1004, name: "Technology" },
];
provide("categoryList", categoryList);
</script>

<style></style>

<template>
  <div id="app">
    <app-header></app-header>
    <router-view></router-view>
    <app-footer></app-footer>
  </div>
</template>
