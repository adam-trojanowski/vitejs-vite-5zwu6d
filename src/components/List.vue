<template>
  <div>
    List
    <ul>
      <li v-for="item in props.items" />
    </ul>
  </div>
</template>

<script lang="ts" setup>
import { type Beer } from "../types"
const props = defineProps<{ items: Beer[] }>()

</script>
