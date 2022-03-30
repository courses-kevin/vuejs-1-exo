<template>
  <div>
    <input type="text" v-model="inputValue" />
    <button @click="handleClick">Ajouter</button>
  </div>
</template>

<script setup>
import { ref, defineEmits } from "vue";

const inputValue = ref("");

const events = defineEmits(["add"]);

const handleClick = () => {
  events("add", inputValue.value);
};
</script>

<style></style>
