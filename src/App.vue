<script setup>
import FancyButton from './components/FancyButton.vue';
</script>

<template>
  <FancyButton> 
    <template v-slot:icon="slotProps">
     {{ slotProps.hover ? '🚀' : '💊' }}
  </template>
  <template v-slot:default>
    <strong 
    style="text-decoration: underline;">E</strong>nviar 📩
  </template> 
    </FancyButton>
    <FancyButton>
      <template #icon="{ hover }">
        {{ hover ? '🚀' : '💊' }}
      </template>
      <template #default>
        <strong 
        style="text-decoration: underline;">C</strong>ancelar
      </template>
    </FancyButton>
</template>

<style scoped>
</style>
