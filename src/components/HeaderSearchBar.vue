<script setup lang="ts"></script>

<style scoped>
.search-box {
  width: 305px;
  height: 40px;
  font-size: 14px;
  text-align: center;
  border-radius: 7px;
  border: 1.5px solid black;
}

.search-icon {
  font-size: 17px;
  font-weight: bolder;
}

.search-button {
  border: 1.5px solid black;
}
</style>

<template>
  <form action="category.html">
    <input
      type="text"
      class="search-box"
      placeholder="Search for Books, Authors and more..."
    />
  </form>
  <div class="search-icon">
    <button class="button search-button">
      <i class="fas fa-search"></i>
    </button>
  </div>
</template>
