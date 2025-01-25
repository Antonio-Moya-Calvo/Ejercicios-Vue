<script setup>
  import TheTitle from'./components/TheTitle.vue'

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="../public/favicon.ico" width="125" height="125" />
  </header>
  <main>
    <h1>Bienvenido a mi Proyecto Vue</h1>
    <TheTitle></TheTitle>
  </main>
</template>

<style scoped>
header {
  width: 100%;
  line-height: 1.5;
  background-color: var(--color-background);
  display: flex;
 flex-direction: row;
 justify-content: center;
}
img{
  margin: auto;
}

h1{
  text-align: center;
  margin: 1em 0;
}

.logo {
  background-color: var(--color-background);
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

}
</style>
