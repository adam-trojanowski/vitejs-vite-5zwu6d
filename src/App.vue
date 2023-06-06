<template>
  <div class="w-full h-full">
    <Header />
    <List :items="beers" />
    <Footer
      @pageChange="(value) => (page = value)"
      :page="page"
      :pageCount="pageCount"
    />
  </div>
</template>

<script setup lang="ts">
  import Header from "./components/Header.vue"
  import List from "./components/List.vue"
  import Footer from "./components/Footer.vue"

  import beerList from "./fixtures/beers.json"
  import { computed, ref } from "vue"

  const page = ref(0)
  const pageSize = ref(3)
  const pageCount = ref(Math.ceil(beerList.length / pageSize.value))

  console.log("pageCount", pageCount.value)

  const beers = computed(() => {
    const start = page.value * pageSize.value
    const end = start + pageSize.value

    return beerList.slice(start, end)
  })
</script>

<style scoped></style>
