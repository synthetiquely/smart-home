<template>
  <div class="section-devices">
    <div class="devices-header">
      <h2 class="subtitle">Избранные устройства</h2>
      <div class="chips">
        <Chip v-for="chip in chips" :key="chip" :text="chip"/>
      </div>
    </div>
    <section class="devices">
      <Feed :horizontal="true" :items="devices" />
    </section>
  </div>
</template>

<script>
import Card from './../Card/Card.vue';
import Icon from './../Icon/Icon.vue';
import Chip from './../Chip/Chip.vue';
import Feed from './../Feed/Feed.vue';
import devices from '../../mocks/devices';

export default {
  components: {
    Card,
    Icon,
    Chip,
    Feed,
  },
  data() {
    return {
      chips: ['Все', 'Кухня', 'Зал', 'Лампочки', 'Камеры'],
      devices,
    };
  },
};
</script>

<style scoped>
.devices-header {
  display: flex;
}

.devices-header > .subtitle {
  margin-right: 15px;
}

.section-devices {
  grid-column: 1 / -1;
  grid-row: 2 / 3;
}

.chips {
  display: flex;
}

.devices {
  overflow: hidden;
}
</style>
