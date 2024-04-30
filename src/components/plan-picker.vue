<template>
    <div ref="plansWrapper"  
    @click="select" class="plans">
      <plan-picker-item
      @select="printSelected"
      :selectedPlan="selectedPlan"
      v-for="plan in plans" 
      :name="plan"
      v-bind:key="plan" />
      <p style="font-size: 25px;">Counter: {{ counter }}</p>
    </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import planPickerItem from './plan-picker-item.vue';
const plans = ref([
  "El soltero",
  "El adicto",
  "El viajero",
  "El colombiano",
  "El italiano"]);

  const plansWrapper = ref (null);

  const selectedPlan = ref(null);

  const printSelected = (playload) => {
    selectedPlan.value = playload;
  }
  
  //Creando una referencia reactiva para un contador
  const counter = ref(0);
  //Creando un metodo para incrementar el contador
  const processId = setInterval(() => {
    console.log('Incrementando contador');
    counter.value++;
  }, 1000);


  //Registrando el CB (Call Back) onMounted
  onMounted(() => {
      //Obteniendo la referencia del elemento .plans
      console.log('Componente Plan Picker Montado');
  console.log(plansWrapper.value);
  });

  //Registrando el CB (Call Back) onUnmounted
  onUnmounted(() => {
      //Obteniendo la referencia del elemento .plans
  console.log('Componente Plan Picker desmontado');
  clearInterval(processId);
  });
</script>