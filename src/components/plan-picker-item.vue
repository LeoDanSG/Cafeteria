<template>
    <div 
    @click="select"
    :class="{'selected-plan':selected}"
    class="plan">
        <div class="description">
            <span class="title">
                {{ name }} {{ selected ? "✔" : "" }}
            </span>
        </div>
      </div>
</template>

<script setup>
import { ref } from 'vue';
//Macro
const emit = defineEmits(['select']);
const props = defineProps({
    name: {
        type: String,
        required: true
    }
});

const selected = ref(false);
const select = () => {
    selected.value = true
    emit('select', props.name);
}

</script>

<style scoped>
.selected-plan {
    background-color: #63dfd0;
}
</style>
