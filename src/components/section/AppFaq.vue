<template>
  <section class="main__faq">
    <div class="container">
      <div class="faq__inner">
        <div class="faq__title">
          <h2>{{ title }}</h2>
        </div>
        <div class="faq__body">
          <app-faq-elem
            v-for="faqElem in faqElems"
            :key="faqElem"
            :faqTitle="faqElem.faqTitle"
            :faqText="faqElem.faqText"
          ></app-faq-elem>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import AppFaqElem from "../elements/AppFaqElem.vue";

export default {
  data() {
    return {
      title: "Вопрос-ответ",
      faqElems: [
        {
          faqTitle:
            "Сколько по времени занимает изготовление пластиковых окон?",
          faqText:
            "Нет, команда мастеров все сами аккуратно доставят и внесут.",
        },
        {
          faqTitle: "Какие существуют способы оплаты?",
          faqText:
            "Нет, команда мастеров все сами аккуратно доставят и внесут.",
        },
        {
          faqTitle: "Где я могу посмотреть образцы?",
          faqText:
            "Нет, команда мастеров все сами аккуратно доставят и внесут.",
        },
        {
          faqTitle: "Зачем вызывать замерщика? Я могу дать размеры",
          faqText:
            "Нет, команда мастеров все сами аккуратно доставят и внесут.",
        },
        {
          faqTitle: "Хотелось бы отделать балкон. Поможете?",
          faqText:
            "Нет, команда мастеров все сами аккуратно доставят и внесут.",
        },
        {
          faqTitle: "Мне надо нанимать грузчиков для подъема?",
          faqText:
            "Нет, команда мастеров все сами аккуратно доставят и внесут.",
        },
      ],
    };
  },
  components: { AppFaqElem },
};
</script>
