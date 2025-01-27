<script setup>
import { ref } from "vue";
import TheTitle from "./TheTitle.vue";

const counter = ref(1);

function increment() {
  counter.value++;
}
function decrement() {
  counter.value--;
}
</script>

<template>
  <section class="section">
    <TheTitle class="section__title"
      >Este contador puede cambiar su valor de forma dinámica</TheTitle
    >
    <div class="section__contador">
      <p>
        El contador tiene un valor de:
        <span class="section__contador__value">{{ counter }}</span>
      </p>
      <p>
        <button v-if="counter < 10" @click="increment">Incrementar</button> o
        <button v-if="counter > 0" @click="decrement">Decrementar</button>
      </p>
      <TheTitle
        v-if="counter >= 10 || counter <= 0"
        class="section__contador__limit"
      >
        HAS LLEGADO AL LÍMITE
      </TheTitle>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.section {
  width: fit-content;
  margin: auto;
  padding: 1em 1em;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.section__contador {
  margin: 1em 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1em;

  &__value {
    font-size: 2em;
    color: var(--color-text-secondary);
  }

  &__limit {
    font-weight: bold;
  }
}
</style>
