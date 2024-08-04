<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import ApplicationHeader from './components/ApplicationHeader.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <ApplicationHeader class="application-header" msg="MedalStat" />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/summer">Summer</RouterLink>
        <RouterLink to="/winter">Winter</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  left: 2.5rem;
  line-height: 1.5;
  max-height: 100vh;
  position: fixed;
  top: 1rem;
  width: 100%;
  display: flex;
  place-items: center;
  padding-right: calc(var(--section-gap) / 2);
}

.wrapper {
  justify-content: space-between;
  width: 100%;
}

nav {
  font-size: 12px;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  border-left: 1px solid var(--color-border);
  display: inline-block;
  padding: 0 1rem;
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    font-size: 1rem;

    left: 2.5rem;
    margin-top: 1rem;
  }
}
</style>
