<template>
  <div class="services__elem" @click="modalActive">
    <div class="services__info">
      <div class="services__top">
        <div class="services__icon">
          <picture>
            <img :src="icon" title="" alt="" width="70" height="75" />
          </picture>
        </div>
        <div class="services__subtitle">
          <h3>{{ subtitle }}</h3>
        </div>
      </div>
      <div class="services__subtext">
        <p>{{ subtext }}</p>
      </div>
    </div>
    <div class="services__img">
      <picture>
        <img :src="image" title="" alt="" width="595" height="268" />
      </picture>
    </div>
    <div class="services__arrow">
      <svg
        width="40"
        height="21"
        viewBox="0 0 40 21"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M23.3846 1.75L38 10.75L23.3846 19.75"
          stroke="white"
          stroke-width="2"
        />
        <path d="M0 10.75H37.0256" stroke="white" stroke-width="2" />
      </svg>
    </div>
  </div>
  <div class="modalBack" :class="isActive ? '_active' : ''">
    <div class="modal">
      <div class="modal__close" @click="modalActive">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="1024"
          height="1024"
          viewBox="0 0 1024 1024"
        >
          <path
            fill="#ef7f1a"
            fill-rule="evenodd"
            d="M799.855 166.312c.023.007.043.018.084.059l57.69 57.69c.041.041.052.06.059.084a.118.118 0 0 1 0 .069c-.007.023-.018.042-.059.083L569.926 512l287.703 287.703c.041.04.052.06.059.083a.118.118 0 0 1 0 .07c-.007.022-.018.042-.059.083l-57.69 57.69c-.041.041-.06.052-.084.059a.118.118 0 0 1-.069 0c-.023-.007-.042-.018-.083-.059L512 569.926L224.297 857.629c-.04.041-.06.052-.083.059a.118.118 0 0 1-.07 0c-.022-.007-.042-.018-.083-.059l-57.69-57.69c-.041-.041-.052-.06-.059-.084a.118.118 0 0 1 0-.069c.007-.023.018-.042.059-.083L454.073 512L166.371 224.297c-.041-.04-.052-.06-.059-.083a.118.118 0 0 1 0-.07c.007-.022.018-.042.059-.083l57.69-57.69c.041-.041.06-.052.084-.059a.118.118 0 0 1 .069 0c.023.007.042.018.083.059L512 454.073l287.703-287.702c.04-.041.06-.052.083-.059a.118.118 0 0 1 .07 0Z"
          />
        </svg>
      </div>
      <div class="modal__top">
        <div class="modal__left">
          <picture>
            <img :src="modalImage" title="" alt="" height="230" width="307" />
          </picture>
        </div>
        <div class="modal__right">
          <div class="modal__title">
            <h3>{{ modalTitle }}</h3>
          </div>
          <div class="modal__text">
            <p>
              {{ modalText }}
            </p>
          </div>
          <div class="mpdal__btns">
            <app-button :href="'#zamer'" :classType="'orange'"
              >Заявка на замер</app-button
            >
            <app-button :href="'#raschet'" :classType="'blue'"
              >Заказать расчет</app-button
            >
          </div>
        </div>
      </div>
      <div class="modal__bottom">
        <div
          class="modal__elem"
          v-for="modalElem in modalElems"
          :key="modalElem"
        >
          <div class="modal__icon">
            <picture>
              <img
                :src="modalElem.elemIcon"
                alt=""
                title=""
                width="80"
                height="70"
              />
            </picture>
          </div>
          <div class="modal__info">
            <div class="modal__subtitle">
              <h4>{{ modalElem.elemSubtitle }}</h4>
            </div>
            <div class="modal__subtext">
              <p>{{ modalElem.elemSubtext }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="modal__img">
        <picture>
          <img
            src="../../../public/img/window-1.webp"
            title=""
            alt=""
            width="450"
            height="470"
          />
        </picture>
      </div>
    </div>
  </div>
</template>

<script>
import AppButton from "./AppButton.vue";

export default {
  props: {
    subtitle: String,
    subtext: String,
    icon: String,
    image: String,
    modalTitle: String,
    modalText: String,
    modalImage: String,
    modalElems: Array,
  },
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    modalActive() {
      this.isActive = !this.isActive;
    },
  },
  components: { AppButton },
};
</script>
