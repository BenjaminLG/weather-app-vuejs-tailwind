

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
  </main>
</template>