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
          <div class="code__item">{{ '<Button' }}</div>
          <div v-if="nameButton !== 'Default'" class="code__item">
            nameButton="{{ nameButton }}"
          </div>
          <div v-if="starIcon" class="code__item">
            starIcon="{{ starIcon }}"
          </div>
          <div v-if="endIcon" class="code__item">endIcon="{{ endIcon }}"</div>
          <div v-if="variant !== 'default'" class="code__item">
            variant="{{ variant }}"
          </div>
          <div v-if="disabledShadow" class="code__item">
            disabledShadow="{{ disabledShadow }}"
          </div>
          <div v-if="size !== 'md'" class="code__item">size="{{ size }}"</div>
          <div v-if="disabled" class="code__item">
            disabled="{{ disabled }}"
          </div>
          <div v-if="color !== 'default'" class="code__item">
            color="{{ color }}"
          </div>
          <div class="code__item">{{ '/>' }}</div>
        </div>
      </code>

      <button
        :class="color, size, { disabled }, { disabledShadow }, variant"
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
        :class="color, size, { disabled }, { disabledShadow }, variant"
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
  background-color: #e0e0e0;
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
  font-weight: 700;
}
/* Default */
.btn--hover-focus {
  background-color: #aeaeae;
}

.btn--hover-focus,
.btn:focus,
.btn:hover {
  background-color: #aeaeae;
}

.btn.outline {
  background-color: transparent;
  border: 1px solid #e0e0e0;
}

.btn--hover-focus.outline,
.btn.outline:hover {
  background: rgb(224, 224, 224, 0.1);
}

.btn.outline .btn__icon,
.btn.outline .btn__name {
  color: #e0e0e0;
}

.btn--hover-focus.text,
.btn.text  {
  color: #e0e0e0;
  background-color: transparent;
  box-shadow: none;
}

.btn--hover-focus.text,
.btn.text:hover {
  background: rgb(224, 224, 224, 0.1);
  color: #e0e0e0;
}
/* Default */

/* Danger */
.danger {
  background-color: #B33771;
  color: #fff;
}

.btn--hover-focus.danger,
.danger:focus,
.danger:hover {
  background-color: #6D214F;
  color: #fff;
}

.danger.outline {
  background-color: transparent;
  border: 1px solid #B33771;
}

.btn--hover-focus.danger.outline,
.danger.outline:hover {
  background: rgb(179, 55, 113, 0.1);
}

.danger.outline .btn__icon,
.danger.outline .btn__name {
  color: #B33771;
}

.btn--hover-focus.danger.text,
.danger.text  {
  color: #B33771;
  background-color: transparent;
  box-shadow: none;
}

.btn--hover-focus.danger.text,
.danger.text:hover {
  background: rgb(179, 55, 113, 0.1);
  color: #B33771;
}
/* Danger */

/* Primary */
.primary {
  background-color: #1B9CFC;
  color: #fff;
}

.btn--hover-focus.primary,
.primary:focus,
.primary:hover {
  background-color: #25CCF7;
  color: #fff;
}

.primary.outline {
  background-color: transparent;
  border: 1px solid #1B9CFC;
}

.btn--hover-focus.primary.outline,
.primary.outline:hover {
  background: rgb(27, 156, 252, 0.1);
}

.primary.outline .btn__icon,
.primary.outline .btn__name {
  color: #1B9CFC;
}

.btn--hover-focus.primary.text,
.primary.text  {
  color: #1B9CFC;
  background-color: transparent;
  box-shadow: none;
}

.btn--hover-focus.primary.text,
.primary.text:hover {
  background: rgb(27, 156, 252, 0.1);
  color: #1B9CFC;
}
/* Primary */

/* Secondary */
.secondary {
  background-color: #182C61;
  color: #fff;
}

.btn--hover-focus.secondary,
.secondary:focus,
.secondary:hover {
  background-color: #3B3B98;
  color: #fff;
}

.secondary.outline {
  background-color: transparent;
  border: 1px solid #182C61;
}

.btn--hover-focus.secondary.outline,
.secondary.outline:hover {
  background: rgb(24, 44, 97, 0.1);
}

.secondary.outline .btn__icon,
.secondary.outline .btn__name {
  color: #182C61;
}

.btn--hover-focus.secondary.text,
.secondary.text  {
  color: #182C61;
  background-color: transparent;
  box-shadow: none;
}

.btn--hover-focus.secondary.text,
.secondary.text:hover {
  background: rgb(24, 44, 97, 0.1);  
  color: #182C61;
}
/* Secondary */

/* Info */
.info {
  background-color: #55E6C1;
  color: #222;
}

.btn--hover-focus.info,
.info:focus,
.info:hover {
  background-color: #58B19F;
  color: #222;
}

.info.outline {
  background-color: transparent;
  border: 1px solid #55E6C1;
}

.btn--hover-focus.info.outline,
.info.outline:hover {
  background: rgba(88, 177, 159 , 0.1);
}

.info.outline .btn__name {
  color: #55E6C1;
}

.btn--hover-focus.info.text,
.info.text  {
  color: #55E6C1;
  background-color: transparent;
  box-shadow: none;
}

.btn--hover-focus.info.text,
.info.text:hover {
  background: rgba(88, 177, 159 , 0.1);
  color: #55E6C1;
}
/* Info */

/* Warning */
.warning {
  background-color: #EAB543;
  color: #222;
}

.btn--hover-focus.warning,
.warning:focus,
.warning:hover {
  background-color: #F8EFBA;
  color: #222;
}

.warning.outline {
  background-color: transparent;
  border: 1px solid #EAB543;
}

.btn--hover-focus.warning.outline,
.warning.outline:hover {
  background: rgb(234, 181, 67, 0.1);
}

.warning.outline .btn__icon,
.warning.outline .btn__name {
  color: #EAB543;
}

.btn--hover-focus.warning.text,
.warning.text  {
  color: #EAB543;
  background-color: transparent;
  box-shadow: none;
}

.btn--hover-focus.warning.text,
.warning.text:hover {
  background: rgb(234, 181, 67, 0.1);
  color: #EAB543;
}
/* Warning */

/* Success */
.success {
  background-color: #26de81;
  color: #222;
}

.btn--hover-focus.success,
.success:focus,
.success:hover {
  background-color: #0fb9b1;
  color: #222;
}

.success.outline {
  background-color: transparent;
  border: 1px solid #26de81;
}

.btn--hover-focus.success.outline,
.success.outline:hover {
  background: rgb(38, 222, 129, 0.1);
}

.success.outline .btn__icon,
.success.outline .btn__name {
  color: #26de81;
}

.btn--hover-focus.success.text,
.success.text  {
  color: #26de81;
  background-color: transparent;
  box-shadow: none;
}

.btn--hover-focus.success.text,
.success.text:hover {
  background: rgb(38, 222, 129, 0.1);
  
  color: #26de81;
}
/* Success */

.btn.disabled {
  pointer-events: none;
  opacity: 0.5;
}

.btn.disabledShadow  {
  box-shadow: none;
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
