<template>
    <div class="plan">
        <div class="description">
            <h1 class="title">
                {{ title }}
            </h1>
        </div>
      </div>
</template>

<script setup>
//Macro
defineProps({
    title: {
        type: String,
        required: true
    }
});
</script>
  