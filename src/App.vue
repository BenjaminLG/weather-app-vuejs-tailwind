<script setup>
import { ref } from 'vue'
import SearchInput from './components/SearchInput.vue'
import WeatherCard from './components/WeatherCard.vue'

const places = ref([]);

const addPlace = (data) => {
  places.value.push(data)
}
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
      <SearchInput @place-data="addPlace"/>
    </article>

    <!-- Weather cards -->
    <article class="grid grid-cols-2 gap-4">
      <div v-for="(place, index) in places" :key="index">
        <WeatherCard :place="place"/>
      </div>
    </article>
  </main>
</template>


