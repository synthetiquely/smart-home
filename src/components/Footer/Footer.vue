<template>
  <footer class="footer">
    <ul class="footer__menu">
      <li class="footer__item">
        <a href="/" class="footer__link">Помощь</a>
      </li>
      <li class="footer__item">
        <a href="/" class="footer__link">Обратная связь</a>
      </li>
      <li class="footer__item">
        <a href="/" class="footer__link">Разработчикам</a>
      </li>
      <li class="footer__item">
        <a href="/" class="footer__link">Условия использования</a>
      </li>
    </ul>
    <div class="footer__legal">
      © 2001–2018  ООО «Яндекс»
    </div>
  </footer>
</template>

<style>
.footer {
  padding: var(--desktop-container-paddings);
  grid-area: footer;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

@media screen (max-width: 768px) {
  .footer {
    padding: var(--mobile-container-paddings);
  }
}

.footer__menu {
  display: flex;
  align-items: center;
  list-style: none;
  margin: 0;
  padding: 0;
}

.footer__item {
  padding: 0 15px;
}

.footer__item:first-of-type {
  padding-left: 0;
}

.footer__link,
.footer__legal {
  font-size: 12px;
  line-height: 14px;
  color: var(--gray);
  letter-spacing: 0.01px;
  text-align: left;
  text-decoration: none;
}
</style>
