<template>
  <header class="header"><slot /></header>
</template>

<style>
.header {
  margin-bottom: 20px;
  padding: var(--desktop-container-paddings);
  grid-area: header;
  display: flex;
  align-items: center;
  border-bottom: 1px solid var(--light-gray);
}

@media screen (max-width: 768px) {
  .header {
    padding: var(--mobile-container-paddings);
  }
}
</style>
