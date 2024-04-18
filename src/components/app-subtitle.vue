<template>
    <div class="plan">
        <div class="description">
            <h2 class="subtitle">
                {{ message }}
            </h2>
        </div>
      </div>
</template>

<script setup>
//Macro
defineProps({
    message: {
        type: String,
        required: true
    }
});
</script>