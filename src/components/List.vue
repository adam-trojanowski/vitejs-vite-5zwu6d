<template>
  <div class="flex content-center flex-row gap-4 w-full flex-wrap">
    <ListItem
      v-for="item in props.items"
      :item="item"
      :key="item.id"
    />
  </div>
</template>

<script lang="ts" setup>
  import { type Beer } from "../types"
  import ListItem from "./ListItem.vue"

  const props = defineProps<{ items: Beer[] }>()
</script>
