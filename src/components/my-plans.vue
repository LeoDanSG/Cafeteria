<template>
    <div class="plan">
      <plan-picker-item 
      v-for="myPlan in plan" 
      :name="myPlan"
      v-bind:key="myPlan" />
    </div>
</template>

<script setup>
import { ref } from 'vue';
import planPickerItem from './plan-picker.vue';
const myPlan = ref([
  "El jubilado",
  "El atratactivo",
  "El bebedor",
  "El astronauto",
  "El dulce"]);
</script>
  