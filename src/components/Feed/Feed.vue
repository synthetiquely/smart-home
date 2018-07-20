<template>
  <section class="feed">
    <Card>
      <p slot="title" class="card__title">
        <Icon temperature />
      </p>
      <p slot="content" class="card__content">Philips Cooler</p>
      <p slot="footer" class="card__footer">Начнет охлаждать в 16:30</p>
    </Card>

    <Card>
      <p slot="title" class="card__title">
        <Icon sun />
      </p>
      <p slot="content" class="card__content">Xiaomi Yeelight LED Smart Bulb</p>
      <p slot="footer" class="card__footer">Включится в 17:00</p>
    </Card>

    <button class="feed__action">
      <Icon double-arrows-up />
    </button>
  </section>
</template>

<script>
import Card from './../Card/Card.vue';
import Icon from './../Icon/Icon.vue';

export default {
  components: {
    Card,
    Icon,
  },
};
</script>

<style scoped>
.feed {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.feed__action {
  position: absolute;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 200px;
  height: 41px;
  background-color: var(--lighten-gray);
  border-radius: 20px 20px 0 0;
  border: none;
  outline-color: var(--dark-yellow);
  transition: all 0.3s ease-out;
  cursor: pointer;
}

.feed__action:hover,
.feed__action:active,
.feed__action:focus {
  background-color: var(--light-gray);
}

.feed__action-reverse {
  top: 0;
  bottom: unset;
  border-radius: 0 0 20px 20px;
}
</style>
