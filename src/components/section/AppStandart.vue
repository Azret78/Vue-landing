<template>
  <section class="main__standart">
    <div class="container">
      <div class="standart__inner">
        <div class="standart__title">
          <picture>
            <img :src="title" alt="" title="" width="300" height="95" />
          </picture>
        </div>
        <div class="standart__body">
          <div
            class="standart__elem"
            v-for="standartElem in standartElems"
            :key="standartElem"
          >
            <div class="standart__img">
              <picture>
                <img
                  :src="standartElem.standartImage"
                  title=""
                  alt=""
                  width="90"
                  height="90"
                />
              </picture>
            </div>
            <div class="standart__subtitle">
              <h3>{{ standartElem.standartTitle }}</h3>
            </div>
          </div>
        </div>
        <div class="standart__back">
          <picture>
            <img :src="background" alt="" title="" width="1200" height="436" />
          </picture>
        </div>
      </div>
      <app-button :class="'blue'">Заказать расчет</app-button>
    </div>
  </section>
</template>

<script>
import AppButton from "../elements/AppButton.vue";

export default {
  data() {
    return {
      title: require("../../../public/svg/standart.svg"),
      background: require("../../../public/img/standart-bg.webp"),
      standartElems: [
        {
          standartImage: require("../../../public/svg/garant-1.svg"),
          standartTitle: "Сертифицированный производитель Rehau",
        },
        {
          standartImage: require("../../../public/svg/garant-2.svg"),
          standartTitle: "Инновационный оконный завод",
        },
        {
          standartImage: require("../../../public/svg/garant-3.svg"),
          standartTitle: "Лидер по переработке профилей Rehau в России",
        },
        {
          standartImage: require("../../../public/svg/garant-4.svg"),
          standartTitle: "Высокотехнологичное автоматизированное оборудование",
        },
        {
          standartImage: require("../../../public/svg/garant-5.svg"),
          standartTitle: "Широкий ассортимент продукции",
        },
      ],
    };
  },
  components: { AppButton },
};
</script>
