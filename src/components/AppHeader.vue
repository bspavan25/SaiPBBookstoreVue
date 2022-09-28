<script setup lang="ts">
import HeaderDropdown from "@/components/HeaderDropdown.vue";
import HeaderSearchBar from "@/components/HeaderSearchBar.vue";
</script>

<style scoped>
header {
  background: var(--secondary-background-color);
  display: flex;
  justify-content: space-between;
  border: 1px solid black;
  align-items: center;
}

.text-logo {
  font-family: var(--title-font-family);
  font-size: 30px;
}

.search-bar {
  display: flex;
  justify-content: space-evenly;
  flex-direction: row;
  width: 305px;
  height: 40px;
  border-radius: 7px;
  gap: 0.2em;
}

.header-dropdown {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  font-size: 15.5px;
}

.login-cart-section {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  font-weight: bolder;
  color: var(--primary-color-dark);
  gap: 0.4em;
}

.login-cart-buttons {
  display: flex;
  flex-direction: row;
  font-size: 17px;
  position: relative;
  align-items: center;
  justify-content: center;
  height: 40px;
}

.cart-icon__badge {
  position: absolute;
  font-size: 12px;
  top: 0.1em;
  right: 10px;
  width: 16px;
  height: 16px;
  background-color: var(--primary-background-color);
  color: black;
  border-radius: 50%;
  justify-content: center;
  align-items: center;
  text-align: center;
  border: 1.5px solid var(--primary-color-dark);
}

.fa-solid {
  margin-right: 8px;
}

@media (max-width: 600px) {
  header {
    flex-direction: column;
  }
}
</style>

<template>
  <header class="container">
    <section class="bookstore-logo">
      <router-link to="/">
        <div class="text-logo">
          <i class="fa-solid fa-book"></i>
          Words n' Pages
        </div>
      </router-link>
    </section>

    <section class="search-bar">
      <header-search-bar></header-search-bar>
    </section>

    <section class="header-dropdown">
      <header-dropdown></header-dropdown>
    </section>

    <section class="login-cart-section">
      <div>
        <button class="button login-cart-buttons">
          <i class="fa-solid fa-user"></i> Login
        </button>
      </div>
      <div>
        <button class="button login-cart-buttons">
          <i class="fa-solid fa-cart-shopping"></i>
          <div class="cart-icon__badge">0</div>
        </button>
      </div>
    </section>
  </header>
</template>
