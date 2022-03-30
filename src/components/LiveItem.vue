<template>
  <li class="toto">
    {{ props.value }}

    <button @click="handleClick">Delete</button>
  </li>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

const props = defineProps(["value"]);

const events = defineEmits(["delete"]);

const handleClick = () => {
  events("delete");
};
</script>

<style></style>
