<script setup>
import { onMounted, ref } from 'vue';

const model = defineModel({
    type: String,
    required: true,
});

const input = ref(null);

onMounted(() => {
    if (input.value.hasAttribute('autofocus')) {
        input.value.focus();
    }
});

defineExpose({ focus: () => input.value.focus() });
</script>

<template>
    <input
        class="rounded-md border-[#acaedb] shadow-sm focus:border-[#F7DFDF] focus:ring-[#F7DFDF]"
        v-model="model"
        ref="input"
    />
</template>
