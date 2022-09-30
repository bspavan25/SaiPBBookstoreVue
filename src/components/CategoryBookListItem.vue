<script setup lang="ts">
import { defineProps } from "vue";
import { BookItem } from "@/types";
const props = defineProps<{
  book: BookItem;
}>();
const bookImageFileName = function (book: BookItem): string {
  let name = book.title.toLowerCase();
  name = name.replace(/ /g, "-");
  name = name.replace(/'/g, "");
  return `${name}.jpeg`;
};
</script>
<style scoped>
.book-box {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: var(--card-background-color);
  max-width: 12em;
  padding: 1em;
  border: 1px solid black;
  text-align: center;
}

.book-image-and-info {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1em;
  padding: 0.4em;
}

.book-image {
  width: 150px;
  height: 230px;
}

.read-now-button {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #0008;
  color: white;
  transform: translateY(-200%);
  margin-bottom: -30%;
  width: 100%;
  height: 30%;
  /*padding: 0.1em;*/
  border-radius: 3px;
  font-size: 170%;
}

.read-now-button:hover {
  cursor: pointer;
  color: var(--primary-background-color);
  font-weight: bold;
  font-size: 190%;
  transform: translateY(-200%);
  margin-bottom: -30%;
  /* background-color: black; */
}

.book-info {
  display: flex;
  flex-direction: column;
  gap: 0.35em;
  align-items: center;
  font-size: 16px;
}

.book-title {
  font-weight: bolder;
  font-size: 18px;
}

.book-price {
  font-style: italic;
  font-size: 15px;
  border: 2px solid red;
  color: black;
  width: 80px;
  height: 20px;
  border-radius: 10px;
}

.add-to-cart {
  display: flex;
  align-items: center;
  justify-content: space-around;
  font-size: 16px;
  font-weight: bolder;
  width: 120px;
  height: 23px;
  border: 1.5px solid black;
  border-radius: 15px;
  padding: 0em 0em;
}
</style>

<template>
  <li class="book-box">
    <div class="book-image-and-info">
      <div class="book-image">
        <img
          :src="require('@/assets/images/books/' + bookImageFileName(book))"
          :alt="book.title"
          style="width: 100%; height: 100%"
        />
        <div v-if="book.readNow == true" class="read-now-button">
          <i class="fa-brands fa-readme"></i>
        </div>
      </div>
      <div class="book-info">
        <div class="book-title">{{ book.title }}</div>
        <div class="book-author">{{ book.author }}</div>
        <div class="book-price">${{ (book.price / 100).toFixed(2) }}</div>
      </div>
      <button class="add-to-cart button">
        Add to Cart
        <i class="fa-solid fa-bag-shopping"></i>
      </button>
    </div>
  </li>
</template>
