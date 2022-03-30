<template>
  <live-form @add="handleAdd" />
  <live-list :items="items" @delete="handleDelete" />
</template>

<script setup>
import { reactive } from "vue";

import LiveList from "./components/LiveList.vue";
import LiveForm from "./components/LiveForm.vue";

const items = reactive(["1", "2", "4"]);

const handleDelete = (key) => {
  items.splice(key, 1);
};

const handleAdd = (value) => {
  items.push(value);
};
</script>
