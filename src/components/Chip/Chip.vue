<template>
  <div tabindex="0" class="chip" @click="$emit('click')">{{text}}</div>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.chip {
  height: 30px;
  margin: 5px;
  padding: 0 15px;
  display: flex;
  align-items: center;
  border-radius: 20px;
  font-size: 13px;
  line-height: 15px;
  font-weight: 600;
  color: var(--black);
  background-color: var(--lighten-gray);
  cursor: pointer;
  outline-color: var(--dark-yellow);
  transition: all 0.3s ease-out;
}

.chip:first-of-type {
  margin-left: 0;
}

..chip:last-of-type {
  margin-right: 0;
}

.chip.active,
.chip:hover,
.chip:active,
.chip:focus {
  background-color: var(--yellow);
}
</style>
