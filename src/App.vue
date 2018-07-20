<template>
  <div id="app">
    <Layout>
      <Header>
        <Logo />
        <HeaderMenu />
      </Header>
      <Content>Content</Content>
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

export default {
  name: 'app',
  components: {
    Layout,
    Header,
    Content,
    Footer,
    HeaderMenu,
    Logo,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono:400,700&subset=cyrillic');

html,
body {
  font-family: 'Roboto Mono', monospace;
  font-size: 18px;
}

body {
  margin: 0;
}
</style>
