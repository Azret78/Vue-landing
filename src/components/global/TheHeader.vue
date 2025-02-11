<template>
  <header class="header">
    <div class="container">
      <div class="header__inner">
        <div class="header__logo">
          <picture>
            <img :src="logo" alt="" title="" width="90" height="63" />
          </picture>
        </div>
        <div class="header__menu">
          <nav class="header__nav">
            <ul class="header__list">
              <li class="header__item" v-for="item in menu" :key="item">
                <a :href="'#' + item.link" class="header__link">
                  {{ item.name }}
                </a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="header__btns">
          <app-button :class="'orange'">Заявка на замер</app-button>
          <app-button :class="'blue'">Заказать расчет</app-button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import AppButton from "../elements/AppButton.vue";

export default {
  data() {
    return {
      logo: require("../../../public/svg/logo.svg"),
      menu: [
        { name: "Услуги", link: "services" },
        { name: "Продукция", link: "product" },
        { name: "О компании", link: "about" },
        { name: "Портфолио", link: "portfolio" },
        { name: "Вопрос-ответ", link: "faq" },
        { name: "Контакты", link: "contact" },
      ],
    };
  },
  components: { AppButton },
};
</script>
