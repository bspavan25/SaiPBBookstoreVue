<script setup lang="ts"></script>

<style scoped>
.home-page {
  display: flex;
}

.welcome-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: var(--primary-color);
  width: 40%;
  border: 1px solid black;
}

.hero-text {
  font-family: var(--title-font-family);
  font-size: 200%;
  color: var(--primary-background-color);
  padding: 1.5em;
  text-align: center;
}

.hero-image {
  border: 1px solid black;
}

.cta-button {
  display: inline-block;
  width: 72%;
  height: 15%;
  background-color: var(--primary-background-color);
  color: var(--primary-color-dark);
  text-decoration: none;
  cursor: pointer;
  border-radius: 15px;
  border: 0px;
  align-items: center;
}

.cta-button:hover {
  width: 72%;
  height: 15%;
  color: var(--secondary-background-color);
  border: 3px solid var(--secondary-background-color);
  background-color: var(--primary-color-dark);
}

.cta-label {
  font-family: var(--title-font-family);
  font-size: 200%;
}

.category-image-items a {
  text-align: center;
  cursor: pointer;
}

.category-image-items div {
  padding: 0.5em 0;
  background: rgba(0, 0, 0, 0.5); /* last # is percent opacity */
  color: white;
  transform: translateY(-2.25em);
  margin-bottom: -2em;
}
</style>
<template>
  <div class="home-page">
    <section class="hero-image">
      <img
        src="../assets/images/site/Curr_Hero_Image.png"
        alt="Words n' Pages hero image"
        width="100%"
        height="100%"
      />
    </section>
    <section class="welcome-text">
      <div class="hero-text">AMAZING eBOOKS FOR GREAT DEALS</div>
      <button class="cta-button">
        <div class="cta-label">SHOP NOW!!</div>
      </button>
    </section>
  </div>
</template>
