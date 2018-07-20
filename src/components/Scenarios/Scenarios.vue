<template>
  <div>
    <h2 class="subtitle">Избранные сценарии</h2>
    <section class="scenarios">

      <div class="scenario">
        <Card>
          <p slot="title" class="card__title">
            <Icon sun-active />
          </p>
          <p slot="content" class="card__content">Выключить весь свет в доме и во дворе</p>
        </Card>
      </div>
      <div class="scenario">
        <Card>
          <p slot="title" class="card__title">
            <Icon time />
          </p>
          <p slot="content" class="card__content">Я ухожу</p>
        </Card>
      </div>
      <div class="scenario">
        <Card>
          <p slot="title" class="card__title">
            <Icon sun-active />
          </p>
          <p slot="content" class="card__content">Включить свет <br> коридоре</p>
        </Card>
      </div>
      <div class="scenario">
        <Card>
          <p slot="title" class="card__title">
            <Icon temperature-active />
          </p>
          <p slot="content" class="card__content">Набрать горячую ванну</p>
          <p slot="footer" class="card__footer">Начнётся в 18:00</p>
        </Card>
      </div>
      <div class="scenario">
        <Card>
          <p slot="title" class="card__title">
            <Icon temperature-active />
          </p>
          <p slot="content" class="card__content">Сделать пол тёплым во всей квартире</p>
        </Card>
      </div>
    </section>
  </div>
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
.scenarios {
  grid-column: 2 / 3;
  grid-row: 1 / 2;
  display: grid;
  grid-template-columns: repeat(auto-fit, 220px);
  grid-auto-rows: 140px;
  grid-auto-flow: dense;
}

.scenario {
  grid-column: span 1;
  grid-row: span 1;
  width: 100%;
  height: 100%;
}
</style>
