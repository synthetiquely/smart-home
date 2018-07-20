<template>
  <button
    :class="{'button': true, 'primary': primary, 'secondary': secondary}"
    @click="$emit('click')"
  >
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    primary: {
      type: Boolean,
      default: false,
      required: false,
    },
    secondary: {
      type: Boolean,
      default: false,
      required: false,
    },
  },
};
</script>

<style scoped>
.button {
  width: 307px;
  height: 60px;
  margin: 0 5px;
  border-radius: 20px;
  color: var(--dark-gray);
  background-color: var(--white);
  text-align: center;
  font-size: 1rem;
  font-weight: 600;
  line-height: 21px;
  letter-spacing: 0;
  cursor: pointer;
  outline-color: var(--dark-yellow);
  border: none;
  transition: all 0.3s ease-out;
}

.button.primary {
  color: var(--black);
  background-color: var(--yellow);
}

.button.primary:hover,
.button.primary:active,
.button.primary:focus {
  background-color: var(--dark-yellow);
}

.button.secondary {
  background-color: var(--lighten-gray);
}

.button.secondary:hover,
.button.secondary:active,
.button.secondary:focus {
  color: var(--black);
  background-color: var(--light-gray);
}
</style>
