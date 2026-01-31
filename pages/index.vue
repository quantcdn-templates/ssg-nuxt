<script setup lang="ts">
useHead({
  title: 'Home - Nuxt Static Site'
})
</script>

<template>
  <main>
    <h1>Welcome to Nuxt 3</h1>
    <p>This is a static site generated with Nuxt 3 and deployed to QuantCDN.</p>

    <section>
      <h2>Features</h2>
      <ul>
        <li>Nuxt 3 with Vue 3</li>
        <li>Static Site Generation</li>
        <li>File-based Routing</li>
        <li>Auto-imports</li>
        <li>TypeScript Support</li>
      </ul>
    </section>

    <section>
      <h2>Getting Started</h2>
      <p>Edit <code>pages/index.vue</code> to start building your site.</p>
    </section>
  </main>
</template>

<style scoped>
main {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  font-family: system-ui, -apple-system, sans-serif;
}

h1 {
  color: #00dc82;
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

h2 {
  color: #1a1a2e;
  font-size: 1.5rem;
  margin-top: 2rem;
  margin-bottom: 0.5rem;
}

p {
  color: #4a4a4a;
  line-height: 1.6;
}

ul {
  list-style-type: disc;
  padding-left: 1.5rem;
  color: #4a4a4a;
}

li {
  margin: 0.5rem 0;
}

code {
  background-color: #f4f4f4;
  padding: 0.2rem 0.4rem;
  border-radius: 4px;
  font-family: monospace;
}

section {
  margin-top: 2rem;
}
</style>
