<template>
  <div
    class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700 m-5"
  >
    <div class="m-2">
      <img
        class="object-contain h-48 w-96"
        :src="props.item.beerImageSrc"
        alt=""
      />
    </div>

    <div class="p-5">
      <h5
        class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
      >
        {{ props.item.beerName }}
      </h5>
      <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
        {{ props.item.beerDescription }}
      </p>
    </div>
  </div>
</template>

<script lang="ts" setup>
  import { Beer } from "../types.ts"

  const props = defineProps<{ item: Beer }>()
</script>
