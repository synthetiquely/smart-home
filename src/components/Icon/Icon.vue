<template>
  <div :class="classes" />
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      required: true,
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
    doubleArrowsUp: {
      type: Boolean,
      default: false,
      required: false,
    },
    doubleArrowsDown: {
      type: Boolean,
      default: false,
      required: false,
    },
  },
  data() {
    return {
      classes: `icon icon__${this.type}`,
    };
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

.icon__double-arrows-up {
  width: 16px;
  height: 16px;
  background-image: url(./../../assets/double_arrows.svg);
}

.icon__double-arrows-down {
  width: 16px;
  height: 16px;
  background-image: url(./../../assets/double_arrows.svg);
  transform: rotate(180deg);
}
</style>
