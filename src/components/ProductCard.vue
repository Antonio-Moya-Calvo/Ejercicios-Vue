<script setup>
import { defineProps } from "vue";
import TheTitle from "./TheTitle.vue";
import productos from "../../data/mock";
</script>

<template>
  <TheTitle class="grid-container__title"
    >Productos de nuestra frutería</TheTitle
  >
  <section class="grid-container__body">
    <div
      v-for="(producto, index) in productos"
      :key="id"
      class="grid-container__item item-card"
    >
      <a :href="producto.imageUrl" target="_blank">
        <div class="item-card__image">
          <img :src="producto.imageUrl" :alt="producto.title" />
        </div>
        <div class="item-card__title">
          <p>{{ producto.title }}</p>
        </div>
        <div class="item-card__description">
          <p>{{ producto.description }}</p>
        </div>
        <div class="item-card__price">
          <p>{{ producto.price }}€ Kg</p>
        </div>
      </a>
    </div>
  </section>
</template>
<style lang="scss" scoped>
.grid-container__body {
  width: 100%;
  background-color: var(--color-background-slider);
  margin: 2em 0;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

.item-card {
  max-width: 20em;
  border: 0.1em solid black;
  background-color: var(--color-background);
  display: flex;
  flex-direction: column;
  gap: 1em;
  margin: 0 1em;

  &__title {
    font-size: 2em;
    font-weight: bold;
    text-align: center;
  }
  &__description {
    color: var(--color-text-primary);
    margin: 0.5em;
  }
  &__price {
    font-size: 2em;
    text-align: center;
  }
}
</style>
