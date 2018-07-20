<template>
  <main class="content"><slot /></main>
</template>

<style>
.content {
  padding: var(--desktop-container-paddings);
  grid-area: content;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
}

@media screen (max-width: 768px) {
  .content {
    padding: var(--mobile-container-paddings);
  }
}
</style>
