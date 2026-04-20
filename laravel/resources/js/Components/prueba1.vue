<script setup>
import { ref, computed } from 'vue';
const title = ref('Variable dinamica');
const num1 = ref(0);
const num2 = ref(0);
const resultado = computed(() => {
    return Number(num1.value) + Number(num2.value);
});

</script>
<style scoped>
</style>
<template>
    <div class="flex items-center justify-center">
        <h1 class="text-black text-4xl font-bold">
            {{ title }}
        </h1>
    </div>
    <div class="flex items-center justify-center mt-4">
        <input v-model="num1" type="number" class="border border-gray-300 rounded px-2 py-1 mr-2" placeholder="Número 1">
        +
        <input v-model="num2" type="number" class="border border-gray-300 rounded px-2 py-1 mr-2" placeholder="Número 2">
        =
        <input v-model="resultado" type="number" class="border border-gray-300 rounded px-2 py-1 mr-2" placeholder="Resultado" readonly>
    </div>
</template>