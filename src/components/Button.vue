<script>
export default {
  props: {
    nameButton: {
      type: String,
      default: 'Default',
    },
    starIcon: {
      type: String,
      default: '',
    },
    endIcon: {
      type: String,
      default: '',
    },
    variant: {
      type: String,
      default: 'default',
    },
    disabledShadow: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    size: {
      type: String,
      default: 'md',
    },
    color: {
      type: String,
      default: 'default',
    },
  },
};
</script>

<template>
  <div class="container">
    <div>
      <code v-if="nameButton">
        <div class="code">
          <div class="code__item">{{ "<Button" }}</div>
          <div v-if="nameButton !=='Default'" class="code__item">nameButton="{{ nameButton }}"</div>
          <div v-if="starIcon" class="code__item">starIcon="{{ starIcon }}"</div>
          <div v-if="endIcon" class="code__item">endIcon="{{ endIcon }}"</div>
          <div v-if="variant !=='default'" class="code__item">variant="{{ variant }}"</div>
          <div v-if="disabledShadow" class="code__item">disabledShadow="{{ disabledShadow }}"</div>
          <div v-if="size !=='md'" class="code__item">size="{{ size }}"</div>
          <div v-if="disabled" class="code__item">disabled="{{ disabled }}"</div>
          <div v-if="color !=='default'" class="code__item">color="{{ color }}"</div>
          <div class="code__item">{{ "/>" }}</div>
        </div>
      </code>
      
      <button
        :class="(color, size, { disabled }, { disabledShadow }, variant)"
        class="btn"
        :disabled="disabled"
      >
        <span v-if="starIcon !== ''" class="btn__icon material-icons">{{
          starIcon
        }}</span>
        <p class="btn__name">{{ nameButton }}</p>
        <span v-if="endIcon !== ''" class="btn__icon material-icons">{{
          endIcon
        }}</span>
      </button>
    </div>

    <div>
      <code>
        <div class="code">
          <div class="code__item">&:hover, &:focus</div>
        </div>
      </code>

      <button
        :class="(color, size, { disabled }, { disabledShadow }, variant)"
        class="btn btn--hover-focus"
        :disabled="disabled"
      >
        <span v-if="starIcon !== ''" class="btn__icon material-icons">{{
          starIcon
        }}</span>
        <p class="btn__name">{{ nameButton }}</p>
        <span v-if="endIcon !== ''" class="btn__icon material-icons">{{
          endIcon
        }}</span>
      </button>
    </div>
  </div>

</template>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1.6rem;
  width: 100%;
  max-width: 600px;
}
.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.4rem;
  padding: 0.8rem 1.6rem;
  border-radius: 0.8rem;
  border: none;
  outline: none;
  cursor: pointer;
  background-color: #E0E0E0;
  box-shadow: 0px 2px 3px rgba(51, 51, 51, 0.2);
  transition: all 0.3s ease;
}

.btn__name {
  font-size: 1.4rem;
  line-height: 2rem;
  font-family: var(--fontFamily1);
  font-weight: 500;
}

.btn__icon {
  font-size: 1.4rem;
  line-height: 1.4rem;
}

.btn--hover-focus {
  background-color: #AEAEAE;
}

.btn:hover {
  background-color: #AEAEAE;
}

.code {
  display: flex;
  align-items: center;
  gap: 0.8rem;
}

.code__item {
  font-size: 1.4rem;
  font-family: var(--fontFamily2);
  margin-bottom: 0.8rem;
}
</style>
