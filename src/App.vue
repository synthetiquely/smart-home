<template>
  <div id="app">
    <Layout>
      <Header>
        <Logo />
        <HeaderMenu />
      </Header>
      <Content>
        <Featured />
        <Scenarios />
        <Devices />

        <Modal v-if="showModal">
          <div slot="header" style="display: flex; justify-content: space-between;">
            <h1 style="margin: 0; font-size: 27px;">Elgato Eve Degree Connected</h1>
            <span>+23</span>
            <Icon type="temperature-active" />
          </div>
          <div slot="content" style="display: flex; flex-direction: column;">
            <p>Включено</p>
            <div style="display: flex;">
              <Chip text="Вручную" />
              <Chip text="Холодно" />
              <Chip text="Тепло" />
              <Chip text="Жарко" />
            </div>
          </div>
          <div slot="footer" style="display: flex;">
            <Button primary>Применить</Button>
            <Button @click="showModal = false">Закрыть</Button>
          </div>
        </Modal>
      </Content>
      <Footer>Footer</Footer>
    </Layout>
  </div>
</template>

<script>
import Layout from './components/Layout/Layout.vue';
import Header from './components/Header/Header.vue';
import HeaderMenu from './components/HeaderMenu/HeaderMenu.vue';
import Logo from './components/Logo/Logo.vue';
import Content from './components/Content/Content.vue';
import Footer from './components/Footer/Footer.vue';
import Button from './components/Button/Button.vue';
import Chip from './components/Chip/Chip.vue';
import Icon from './components/Icon/Icon.vue';
import Card from './components/Card/Card.vue';
import Modal from './components/Modal/Modal.vue';
import Featured from './components/Featured/Featured.vue';
import Scenarios from './components/Scenarios/Scenarios.vue';
import Devices from './components/Devices/Devices.vue';

export default {
  name: 'app',
  components: {
    Layout,
    Header,
    Content,
    Footer,
    HeaderMenu,
    Logo,
    Button,
    Chip,
    Icon,
    Card,
    Modal,
    Featured,
    Scenarios,
    Devices,
  },
  data() {
    return {
      showModal: false,
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono:400,700&subset=cyrillic');

:root {
  --gray: #858585;
  --light-gray: #f0f0f0;
  --lighten-gray: #f7f7f7;
  --dark-gray: #333;
  --yellow: #ffd93e;
  --dark-yellow: #ffcd00;
  --white: #fff;
  --black: #000;
  --desktop-container-paddings: 0 30px;
  --mobile-container-paddings: 0 15px;
}

html,
body {
  height: 100%;
  font-family: 'Roboto Mono', monospace;
  font-size: 18px;
}

#app {
  height: 100%;
}

body {
  margin: 0;
}

a,
button,
input {
  outline-color: var(--dark-yellow);
}

p {
  margin: 0;
  color: var(--dark-gray);
  font-size: 14px;
  line-height: 16px;
  font-weight: 400;
}

span {
  color: var(--gray);
  font-size: 14px;
  line-height: 16px;
  font-weight: 400;
}

.title {
  margin: 0;
  padding: 10px 0;
  color: var(--dark-gray);
  font-size: 27px;
  line-height: 31px;
  font-weight: 600;
}

.subtitle {
  margin: 0;
  padding: 10px 0;
  color: var(--dark-gray);
  font-size: 18px;
  line-height: 21px;
  font-weight: 600;
}
</style>
