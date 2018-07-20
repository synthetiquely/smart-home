<template>
  <section class="featured">

    <div class="featured__meta">
      <h1 class="title">Привет, Геннадий!</h1>
      <p class="description">Двери и окна закрыты, сигналиация включена.</p>

      <div class="temperature-stats">
        <div class="temperature-stats__item">
          <span>Дома</span>
          <span class="temperature-stats__data">+23</span>
        </div>
        <div class="temperature-stats__item">
          <span>За окном</span>
          <span class="temperature-stats__data">+19&nbsp;<Icon cloud/></span>
        </div>
      </div>
    </div>

    <div class="featured__feed">
      <Feed />
    </div>
  </section>
</template>

<script>
import Feed from './../Feed/Feed.vue';
import Icon from './../Icon/Icon.vue';

export default {
  components: {
    Feed,
    Icon,
  },
};
</script>

<style scoped>
.featured {
  width: 600px;
  height: 301px;
  padding: 15px;
  display: grid;
  grid-template-rows: auto auto auto;
  grid-template-columns: auto 200px;
  background-image: url(./../../assets/bg@2x.png);
  background-size: cover;
  background-repeat: no-repeat;
}

.featured__meta {
  grid-column: 1 / 2;
  grid-row: 1 / -1;
}

.featured__feed {
  grid-column: 2 / -1;
  grid-row: 1 / -1;
  margin: -15px 0;
  overflow-y: visible;
}

.temperature-stats {
  padding-top: 20px;
  display: flex;
}

.temperature-stats__item {
  padding: 0 15px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.temperature-stats__item:first-of-type {
  padding-left: 0;
}

.temperature-stats__item:last-of-type {
  padding-right: 0;
}

.temperature-stats__data {
  display: flex;
  align-items: center;
  color: var(--dark-gray);
  font-size: 36px;
  line-height: 42px;
  font-weight: 600;
  letter-spacing: 0;
}
</style>
