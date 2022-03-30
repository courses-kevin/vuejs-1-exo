<template>
  <ul>
    <live-item
      v-for="(item, key) in props.items"
      :key="key"
      :value="item"
      @delete="() => handleDelete(key)"
    />
  </ul>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

import LiveItem from "./LiveItem.vue";

const props = defineProps(["items"]);

const events = defineEmits(["delete"]);

const handleDelete = (key) => {
  console.log("DELETE", key);
  events("delete", key);
};
</script>

<style></style>
