<template>
    <div @click="select" class="plans">
      <plan-picker-item
      @select="printSelected"
      v-for="plan in plans" 
      :name="plan"
      v-bind:key="plan" />
      {{ selectedPlan }}
    </div>
</template>

<script setup>
import { ref } from 'vue';
import planPickerItem from './plan-picker-item.vue';
const plans = ref([
  "El soltero",
  "El adicto",
  "El viajero",
  "El colombiano",
  "El italiano"]);

  const selectedPlan = ref(null);

  const printSelected = (playload) => {
    selectedPlan.value = playload;
  }
</script>