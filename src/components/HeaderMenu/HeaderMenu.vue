<template>
  <nav class="navigation">
    <ul class="navigation__menu">
      <li class="navigation__item">
        <a class="navigation__link" href="/">Сводка</a>
      </li>
      <li class="navigation__item">
        <a class="navigation__link" href="/">Устройства</a>
      </li>
      <li class="navigation__item">
        <a class="navigation__link" href="/">Сценарии</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.navigaton {
  width: 100%;
}

.navigation__menu {
  width: 100%;
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.navigation__item {
  padding: 0 15px;
}

.navigation__link {
  font-size: 16px;
  line-height: 20px;
  font-weight: 600;
  color: var(--dark-gray);
  opacity: 0.6;
  text-decoration: none;
}

.navigation__link:hover,
.navigation__link:active,
.navigation__link:focus,
.navigation__link.active {
  opacity: 1;
}
</style>
