<script setup>
import { ref } from 'vue'
import TheTitle from './TheTitle.vue'

const counter = ref(0)

function increment() { counter.value++ }
function decrement() { counter.value-- }

</script>

<template>
<section>
<TheTitle>Este contador puede cambiar su valor de forma dinámica </TheTitle>
<div class="contador">
    <p>El contador tiene un valor de: <span>{{ counter }}</span> </p>
    <p><button v-if="(counter < 10)" @click="increment">Incrementar</button> o <button v-if="(counter > 0)" @click="decrement">Decrementar</button></p>
    <TheTitle v-if="(counter >= 10 || counter <= 0)">HAS LLEGADO AL LÍMITE</TheTitle>
</div>
</section>
</template>

<style>
    section {
        width:fit-content;
        margin: auto;
        padding: 1em 1em;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .contador{
        margin: 1em 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1em;
    }
    span{
        font-size: 2em;
        color: var(--color-text-secondary);
    }


</style>