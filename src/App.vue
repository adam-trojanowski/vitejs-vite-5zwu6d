<script setup lang="ts">
import Header from './components/Header.vue';
import List from './components/List.vue';
import Footer from './components/Footer.vue';

import beerList from './fixtures/beers.json';
</script>

<template>
  <div class="w-full h-full">
    <Header />
    <List :items="beerList" />
    <Footer />
  </div>
</template>

<style scoped></style>
