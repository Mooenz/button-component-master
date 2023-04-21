<script setup>
import Button from './components/Button.vue';

</script>

<template>
  <section class="section">
    <h1 class="title">Buttons</h1>

    <section class="section__buttons">
      <Button />
      <Button disabled />
      <Button starIcon="add_shopping_cart" />

      <Button starIcon="west" nameButton="Back" color="primary"/>
      <Button endIcon="expand_more" nameButton="More" color="secondary"/>
      <Button endIcon="east" nameButton="Go" color="danger"/>

      <Button nameButton="Sing in" color="info" variant="outline"/>
      <Button starIcon="add" nameButton="Create" color="warning" variant="outline"/>
      <Button starIcon="emoji_events" nameButton="My favorites" color="success" variant="outline"/>

      <Button nameButton="Click Here" color="primary" variant="text" disabledShadow/>
      <Button nameButton="Click Here" variant="text" disabledShadow/>
      <Button nameButton="Click Here" color="danger" variant="text" disabledShadow/>
      
    </section>
  </section>
</template>

<style scoped>

.section {
  padding: 4rem 2.4rem;
  width: 100%;
  max-width: 120rem;
  margin: 0 auto;
}

.section__buttons {
  display: flex;
  flex-direction: column;
  gap: 2.4rem;
}

.title {
  font-size: 3rem;
  font-weight: 600;
  font-family: var(--fontFamily1);
  margin-bottom: 2.4rem;
}
</style>
