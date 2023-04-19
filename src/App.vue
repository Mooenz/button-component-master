<script setup>
import Button from './components/Button.vue';
</script>

<template>
  <section class="section">
    <h1 class="title">Buttons</h1>

    <section class="section__buttons">
      <Button />
      <Button starIcon="add_shopping_cart" />
    </section>
  </section>
</template>

<style scoped>
.section {
  padding: 7rem 2.4rem;
  width: 100%;
  max-width: 120rem;
  margin: 0 auto;
}
.section__buttons {
  display: flex;
  flex-direction: column;
  gap: 2.4rem;
  /* grid-template-columns: repeat(2, 1fr); */
}

.title {
  font-size: 3rem;
  font-weight: 600;
  font-family: var(--fontFamily1);
  margin-bottom: 2.4rem;
}
</style>
