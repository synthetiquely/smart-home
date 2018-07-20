<template>
  <main class="content"><slot /></main>
</template>

<style>
.content {
  padding: var(--desktop-container-paddings);
  grid-area: content;
}

@media screen (max-width: 768px) {
  .content {
    padding: var(--mobile-container-paddings);
  }
}
</style>
