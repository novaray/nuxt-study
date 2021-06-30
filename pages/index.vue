<template>
  <div class="container">
    <div>
      <nav>
        <ul>
          <li>
            <NuxtLink to="/loading">Loading</NuxtLink>
          </li>
        </ul>
      </nav>
      <main>
        <Logo />
        <h1 class="title">
          my-nuxt
        </h1>
      </main>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({

})
</script>

<style>
:root {
  --primary-color: #00c58e;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

a,
a:visited {
  text-decoration: none;
  color: inherit;
}

a:hover,
a.nuxt-link-exact-active {
  color: var(--primary-color);
}

main {
  margin: 0 auto;
  margin-top: 25vh;
  margin-bottom: 2rem;
  padding: 0 1rem;
  max-width: 1280px;
  text-align: center;
}

nav {
  padding: 0 1rem;
}

ul {
  list-style-type: none;
  padding: 0;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

li {
  margin: 0 0.5rem;
  padding: 0.25rem;
  font-size: 1.2rem;
}
</style>
