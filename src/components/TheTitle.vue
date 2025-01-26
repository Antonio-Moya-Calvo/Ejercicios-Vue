<script setup>
import { defineProps } from 'vue'
    const props = defineProps(['propTitle'])
</script>
<template>
    <h2>{{ props.propTitle }}</h2>
</template>
<style scoped>
    h2{
        margin: auto;
        text-align: center;
        color: var(--color-text-secondary);
    }
</style>