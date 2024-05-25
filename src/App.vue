<script setup>

import SearchInput from './components/SearchInput.vue'


</script>

<template>
  <main>
    <!-- Date -->
    <article class="text-center mb-6">
    {{ new Date().toLocaleDateString('fr-FR', {
      weekday: 'long',
      year: 'numeric',
      month: 'long',
      day: 'numeric',
    }) }}
    </article>
    <!-- Search -->
    <article>
      <searchInput/>
    </article>
  </main>
</template>