<template>
  <div class="card">
    <slot name="title"/>
    <slot name="content"/>
    <slot name="footer"/>
  </div>
</template>

<style scoped>
.card {
  width: 170px;
  height: 90px;
  padding: 15px;
  margin: 10px;
  display: flex;
  flex-direction: column;
  background-color: var(--lighten-gray);
  border-radius: 20px;
  cursor: pointer;
  transition: all 0.3s ease-out;
}

@media screen and (max-width: 1200px) {
  .card {
    height: 120px;
  }
}

.card:hover,
.card:active,
.card:focus,
.card.active {
  background-color: var(--white);
  box-shadow: 0 2px 6px rgba(197, 186, 186, 0.5);
}

.card__title {
  margin-bottom: 15px;
}

.card__content {
  flex: 1;
  font-size: 14px;
  font-weight: 600;
  line-height: 16px;
  color: var(--dark-gray);
}

.card__footer {
  font-size: 12px;
  line-height: 14px;
  color: var(--gray);
}
</style>
