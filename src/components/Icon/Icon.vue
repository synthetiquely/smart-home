<template>
  <div
    :class="{
      'icon': true,
      'icon__sun': sun,
      'icon__temperature': temperature,
      'icon__time': time,
      'icon__cloud': cloud,
      'icon__sun-active': sunActive,
      'icon__temperature-active': temperatureActive
    }"
  />
</template>

<script>
export default {
  props: {
    sun: {
      type: Boolean,
      default: false,
      required: false,
    },
    temperature: {
      type: Boolean,
      default: false,
      required: false,
    },
    sunActive: {
      type: Boolean,
      default: false,
      required: false,
    },
    temperatureActive: {
      type: Boolean,
      default: false,
      required: false,
    },
    time: {
      type: Boolean,
      default: false,
      required: false,
    },
    cloud: {
      type: Boolean,
      default: false,
      required: false,
    },
  },
};
</script>

<style scoped>
.icon {
  width: 24px;
  height: 24px;

  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}

.icon__sun {
  background-image: url(./../../assets/icon_sun.svg);
}

.icon__sun-active {
  background-image: url(./../../assets/icon_sun_active.svg);
}

.icon__time {
  background-image: url(./../../assets/icon_time.svg);
}

.icon__temperature {
  background-image: url(./../../assets/icon_temperature.svg);
}

.icon__temperature-active {
  background-image: url(./../../assets/icon_temperature_active.svg);
}

.icon__cloud {
  width: 26px;
  height: 26px;
  background-image: url(./../../assets/icon_cloud.svg);
}
</style>
