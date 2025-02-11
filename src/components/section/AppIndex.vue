<template>
  <section class="main__index">
    <div class="container">
      <div class="index__inner">
        <div class="index__left">
          <div class="index__title">
            <h1>
              <span>{{ title.span }}</span
              >{{ title.default }}
            </h1>
          </div>
          <div class="index__elems">
            <app-elem
              v-for="elem in elems"
              :key="elem.text"
              :text="elem.text"
              :src="elem.src"
            ></app-elem>
          </div>
        </div>
        <div class="index__form">
          <h4>
            {{ formTitle }}
          </h4>
          <form :aria-label="formTitle" @submit.prevent="submitHandler">
            <div class="index__pole">
              <app-input
                type="text"
                placeholder="Представьтесь, пожалуйста"
                v-model:value="name"
                :error="errors.name"
              ></app-input>
            </div>
            <div class="index__pole">
              <app-input
                type="tel"
                placeholder="Номер телефона"
                v-model:value="tel"
                :error="errors.tel"
              ></app-input>
            </div>
            <div class="index__pole">
              <app-input
                type="email"
                placeholder="E-mail"
                v-model:value="mail"
              ></app-input>
            </div>
            <div class="index__pole">
              <input type="submit" value="Отправить заявку" />
            </div>
          </form>
          <div class="index__image">
            <picture>
              <img
                src="../../../public/img/metr.webp"
                title=""
                alt=""
                width="444"
                height="65"
              />
            </picture>
          </div>
        </div>
      </div>
    </div>
    <div class="index__background">
      <picture>
        <img
          src="../../../public/img/main.webp"
          title=""
          alt=""
          width="1920"
          height="562"
        />
      </picture>
    </div>
  </section>
</template>

<script>
import AppElem from "../elements/AppElem.vue";
import AppInput from "../elements/AppInput.vue";

export default {
  data() {
    return {
      title: {
        span: "Окна Хаус -",
        default: "Профессиональный подход к остеклению",
      },
      elems: [
        {
          text: "Современные окна и балконные конструкции по доступным ценам",
          src: require("../../../public/svg/icon-1.svg"),
        },
        {
          text: "Квалифицированный подход к решению задач любой сложности",
          src: require("../../../public/svg/icon-2.svg"),
        },
        {
          text: "Гарантия высочайшего качества нашей продукции",
          src: require("../../../public/svg/icon-3.svg"),
        },
      ],
      formTitle: "Вызвать замершика на дом",
      name: "",
      tel: "",
      mail: "",
      errors: {
        name: null,
        tel: null,
      },
    };
  },
  methods: {
    isFormValid() {
      let isValid = true;
      if (this.name.length === 0) {
        this.errors.name = "Введите ваше имя";
        isValid = false;
      } else {
        this.errors.name = "";
      }
      if (this.tel.length === 0) {
        this.errors.tel = "Введите номер телефона";
        isValid = false;
      } else {
        this.errors.tel = "";
      }
      return isValid;
    },
    submitHandler() {
      if (this.isFormValid()) {
        console.log(this.name);
        console.log(this.tel);
        console.log(this.mail);
      }
    },
  },
  components: { AppElem, AppInput },
};
</script>
