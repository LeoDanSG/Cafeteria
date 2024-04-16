<template>
    <div class="plan">
        <div class="description">
            <span class="title">
                {{ name }} 👍 Likes: {{ likes }}
            </span>
        </div>
      </div>
</template>

<script setup>
//Macro
defineProps({
    name: {
        type: String,
        required: true,
    },
    likes: {
        type: Number,
        default: 0,
    }
});
</script>
