<template>
  <section :class="{'horizontal': horizontal}" class="feed">
    <Card v-for="item in items" :key="item.title">
      <p v-if="item.icon" slot="title" class="card__title">
        <Icon :type="item.icon" />
      </p>
      <p v-if="item.title" slot="content" class="card__content">{{item.title}}</p>
      <p v-if="item.status" slot="footer" class="card__footer">{{item.status}}</p>
    </Card>
    <button class="feed__action">
      <Icon type="double-arrows-up"  />
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
  props: {
    horizontal: {
      type: Boolean,
      default: false,
      required: false,
    },
    items: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.feed {
  position: relative;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.feed.horizontal {
  flex-direction: row;
}

.feed.horizontal > .feed__action {
  display: none;
  visibility: hidden;
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
