<template>
  <section class="main__about">
    <div class="container">
      <div class="about__inner">
        <div class="about__title">
          <h2>{{ title }}</h2>
        </div>
        <app-description
          :descriptionLogo="description.descriptionLogo"
          :descriptionText="description.descriptionText"
          :descriptionPoster="description.descriptionPoster"
        />
        <app-work :title="work.title" :elems="work.elems" />
        <app-feedback
          :slides="feedback.slides"
          :activeIndex="activeIndex"
          @prev="prev"
          @next="next"
          :formName="formName"
          :formDogovor="formDogovor"
          :formText="formText"
          :formTitle="formTitle"
        />
        <div class="about__body">
          <div
            class="about__elem"
            v-for="aboutElem in aboutElems"
            :key="aboutElem"
          >
            <div class="about__elem-img">
              <picture>
                <img
                  :src="aboutElem.aboutImage"
                  title=""
                  alt=""
                  width="85"
                  height="80"
                />
              </picture>
            </div>
            <div class="about__elem-info">
              <div class="about__elem-title">
                <h3>{{ aboutElem.aboutTitle }}</h3>
              </div>
              <div class="about__elem-text">
                <p>{{ aboutElem.aboutText }}</p>
              </div>
            </div>
          </div>
        </div>
        <app-button :class="'orange'">Оформить заявку на замер</app-button>
      </div>
    </div>
  </section>
</template>

<script>
import AppButton from "../elements/AppButton.vue";
import AppDescription from "../elements/AppDescription.vue";
import AppFeedback from "../elements/AppFeedback.vue";
import AppWork from "../elements/AppWork.vue";

export default {
  data() {
    return {
      title: "О компании",
      aboutMenu: [
        { id: 1, aboutItem: "Описание" },
        { id: 2, aboutItem: "Как мы работаем" },
        { id: 3, aboutItem: "Отзывы" },
      ],
      aboutElems: [
        {
          aboutImage: require("../../../public/svg/about-1.svg"),
          aboutTitle: "профессионализм",
          aboutText:
            "Бригада профессиональных мастеров по монтажу и обслуживанию",
        },
        {
          aboutImage: require("../../../public/svg/about-2.svg"),
          aboutTitle: "Ценообразование",
          aboutText: "Лучшие цены на рынке пластиковых окон",
        },
        {
          aboutImage: require("../../../public/svg/about-3.svg"),
          aboutTitle: "Мобильность",
          aboutText: "Заключение договора на дому",
        },
        {
          aboutImage: require("../../../public/svg/about-4.svg"),
          aboutTitle: "Лояльность",
          aboutText: "99% клиентов рекомендуют нас своим друзьям",
        },
        {
          aboutImage: require("../../../public/svg/about-5.svg"),
          aboutTitle: "Скорость",
          aboutText: "Короткие сроки установки изделий",
        },
        {
          aboutImage: require("../../../public/svg/about-6.svg"),
          aboutTitle: "Служба качества",
          aboutText: "Безупречное качество и контроль изделий ПВХ",
        },
      ],
      description: {
        descriptionLogo: require("../../../public/svg/logo.svg"),
        descriptionText:
          "Мы помогаем клиентам подбирать решения, учитывая пожежелания к характеристикам окна и его стоимости. Окно - это объект, которым Вы будете пользоваться много лет, поэтому для нас очень важно, чтобы Вы сделали правильный выбор.",
        descriptionPoster: require("../../../public/img/video.webp"),
      },
      work: {
        title: "Как мы работаем",
        elems: [
          {
            workImage: require("../../../public/svg/work-1.svg"),
            workTitle: "Бесплатно приедем",
            workText: "Выезжаем бесплатно во все города Московской области",
          },
          {
            workImage: require("../../../public/svg/work-2.svg"),
            workTitle: "Выезжаем ежедневно",
            workText: "С 9 до 21 без выходных и праздников",
          },
          {
            workImage: require("../../../public/svg/work-3.svg"),
            workTitle: "Образцы с собой",
            workText: "Покажем образцы профильных систем и материалов отделки",
          },
          {
            workImage: require("../../../public/svg/work-4.svg"),
            workTitle: "Стоимость",
            workText: "Называем точную стоимость заказа на месте",
          },
        ],
      },
      feedback: {
        slides: [
          {
            id: 1,
            name: "Раиса Михайлола",
            date: "24.06.2021",
            dogovor: "123456",
            text: "Огромное СПАСИБО всей команде Дизайн-Окно! В июне 2021 заказывала переостекление + отделка балкона первый раз и так все удачно - быстро, качественно. Все прошло отлично, в соответствии с условиями договора. Замерщик приехал как оговорено без опозданий, произвел замер лазерным уровнем, все подробно рассказал по профилю и комплектующим. Предоплата составила 20%, остаток - по факту. Соотношение цена/качество в сравнении с конкурентами. Доставка точно в срок, за 3 дня все установили. Итог - красивые окна. Будем зимой проверять на прочность :) Большая благодарность за отлично проведённую работу! Замерщик по вызову пришёл быстро, всё хорошо объяснил , окна пришли в соответствии со согласованной датой, поднятие в квартиру прошла очень хорошо ,  монтажники справились со своей работой на отлично!  Все прошло в позитиве, соотношение цены и качества хорошее. Отличная команда! Спасибо!!!",
          },
          {
            id: 2,
            name: "Анаиса",
            date: "24.06.2021",
            dogovor: "123456",
            text: "Огромное СПАСИБО всей команде Дизайн-Окно! В июне 2021 заказывала переостекление + отделка балкона первый раз и так все удачно - быстро, качественно. Все прошло отлично, в соответствии с условиями договора. Замерщик приехал как оговорено без опозданий, произвел замер лазерным уровнем, все подробно рассказал по профилю и комплектующим. Предоплата составила 20%, остаток - по факту. Соотношение цена/качество в сравнении с конкурентами. Доставка точно в срок, за 3 дня все установили. Итог - красивые окна. Будем зимой проверять на прочность :)",
          },
          {
            id: 3,
            name: "Раиса",
            date: "24.06.2021",
            dogovor: "123456",
            text: "Большая благодарность за отлично проведённую работу! Замерщик по вызову пришёл быстро, всё хорошо объяснил , окна пришли в соответствии со согласованной датой, поднятие в квартиру прошла очень хорошо ,  монтажники справились со своей работой на отлично!  Все прошло в позитиве, соотношение цены и качества хорошее. Отличная команда! Спасибо!!!",
          },
        ],
      },
      activeIndex: 0,
    };
  },
  methods: {
    next() {
      if (this.activeIndex !== this.feedback.slides.length - 1) {
        this.activeIndex++;
      }
    },
    prev() {
      if (this.activeIndex !== 0) {
        this.activeIndex--;
      }
    },
  },
  computed: {
    activeStep() {
      return this.feedback.slides[this.activeIndex];
    },
  },
  components: { AppButton, AppDescription, AppWork, AppFeedback },
};
</script>
