<script setup lang="ts"></script>

<style scoped>
footer {
  background: var(--secondary-background-color);
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  border: 1px solid black;
}
.footer-main-frame {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0.9em;
}

.social-media-icons {
  display: flex;
  flex-direction: row;
  font-size: 27px;
  font-weight: bolder;
  gap: 0.6em;
  color: var(--primary-color-dark);
}

.signup-and-links {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5em;
}

.news-letter-button {
  font-family: var(--title-font-family);
  font-size: 17px;
  background-color: var(--primary-color-dark);
  color: var(--secondary-background-color);
  padding: 0.4em 0.4em;
}

.news-letter-button:hover {
  color: var(--primary-color-dark);
  background-color: var(--secondary-background-color);
  border: 2px solid var(--primary-color-dark);
}

.about-links {
  font-size: 15px;
  color: var(--primary-color-dark);
}

.address-part {
  display: flex;
  flex-direction: column;
  text-align: right;
}

.copy-rights-bar {
  display: flex;
  background-color: var(--primary-color-dark);
  height: 1.4em;
  border: 1px solid black;
  font-size: 14px;
  color: var(--primary-background-color);
  align-items: center;
  justify-content: center;
}
</style>

<template>
  <footer>
    <section class="footer-main-frame">
      <div>
        <section class="social-media-icons links">
          <i class="fa-brands fa-facebook"></i>
          <i class="fa-brands fa-twitter"></i>
          <i class="fa-brands fa-linkedin"></i>
          <i class="fa-brands fa-instagram"></i>
        </section>
      </div>
      <div class="signup-and-links">
        <section>
          <button class="news-letter-button button">
            SIGN UP - News Letter
          </button>
        </section>
        <section class="about-links links">
          <router-link to="/"> About </router-link> |
          <router-link to="/"> Privacy </router-link> |
          <router-link to="/"> Terms </router-link> |
          <router-link to="/"> Help </router-link> |
          <router-link to="/">Contact </router-link>
        </section>
      </div>
      <div class="address-part">
        <div>
          <i class="fa-solid fa-location-pin"></i> Stroubles Creek<br />
          Blacksburg<br />
          VA 24060
        </div>
      </div>
    </section>
    <section class="copy-rights-bar">
      <i class="fa-regular fa-copyright"></i>
      All Rights Reserved.
    </section>
  </footer>
</template>
