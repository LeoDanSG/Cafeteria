<script setup>
import planPicker from './components/plan-picker.vue';
import appTitle from './components/app-title.vue';
import appSubtitle from './components/app-subtitle.vue';
import myPlans from './components/my-plans.vue';
</script>

<template>
  <header>
    <div>
      <span id="logo">Liquid Gold Box</span>
      <img src="./assets/logo.png" alt="logo">
    </div>
  </header>

  <div class="content">

    <!-- <app-title title="Coffee Plans" />-->
    <app-title title="Planes de Viaje" />
    <!-- <app-subtitle message="Viajamos por el mundo para encontrar el mejor café de origen único para ti" />-->
    <app-subtitle message="Vamos por el mundo para encontrar el mejor café de origen único para ti" />

    <!-- my-plans es una arreglo reactivo de planes"-->
      <!-- <plan-picker :plans="my-plans" />-->
    <plan-picker :plans="myPlans" />
  
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
