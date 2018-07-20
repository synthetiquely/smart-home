<template>
  <div id="app">
    <Layout>
      <Header>
        <Logo />
        <HeaderMenu />
      </Header>
      <Content>
        <Button primary>Применить</Button>
        <Button secondary>Применить</Button>
        <Button>Закрыть</Button>
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
  font-family: 'Roboto Mono', monospace;
  font-size: 18px;
}

body {
  margin: 0;
}
</style>
