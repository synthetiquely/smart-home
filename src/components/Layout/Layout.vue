<template>
  <div class="layout"><slot /></div>
</template>

<style>
.layout {
  display: grid;
  grid-template-columns: auto;
  grid-template-rows: 120px auto 50px;
  grid-template-areas:
    'header'
    'content'
    'footer';
}
</style>
