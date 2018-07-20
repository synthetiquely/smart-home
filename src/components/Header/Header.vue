<template>
  <header class="header"><slot /></header>
</template>

<style>
.header {
  margin-bottom: 20px;
  padding: 0 30px;
  grid-area: header;
  display: flex;
  align-items: center;
  border-bottom: 1px solid #f0f0f0;
}
</style>
