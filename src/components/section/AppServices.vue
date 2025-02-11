<template>
  <section class="main__services">
    <div class="container">
      <div class="services__inner">
        <div class="services__title">
          <h2>
            {{ title }}
          </h2>
        </div>
        <div class="services__body">
          <app-service
            v-for="service in services"
            :key="service"
            :subtitle="service.subtitle"
            :subtext="service.subtext"
            :icon="service.icon"
            :image="service.image"
            :modalTitle="service.modalTitle"
            :modalText="service.modalText"
            :modalImage="service.modalImage"
            :modalElems="service.modalElems"
          ></app-service>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import AppService from "../elements/AppService.vue";

export default {
  data() {
    return {
      title: "Наши услуги",
      services: [
        {
          subtitle: "Установка пластиковых окон",
          subtext:
            "Устанавливаем пластиковые окна Rehau от проверенного производителя с гарантией качества",
          icon: require("../../../public/svg/service-1.svg"),
          image: require("../../../public/img/service-1.webp"),
          modalTitle: "Установка пластиковых окон",
          modalText:
            "Пластиковые окна Rehau от проверенного производителя с гарантией качества",
          modalImage: require("../../../public/img/slide-1.webp"),
          modalElems: [
            {
              elemSubtitle: "Пластиковые окна",
              elemSubtext:
                "Использование ламинационных окон, ламинации в массе, 3д-ламинации, а также покраска окон.",
              elemIcon: require("../../../public/svg/window-1.svg"),
            },
            {
              elemSubtitle: "Ламинация",
              elemSubtext:
                "Пластиковые окна могут быть любого нужного вам цвета. Внутри и снаружи. ",
              elemIcon: require("../../../public/svg/window-2.svg"),
            },
            {
              elemSubtitle: "Подоконники",
              elemSubtext:
                "Качественный подоконник не царапается, выдерживает большие нагрузки и будет служить вам долгие годы. ",
              elemIcon: require("../../../public/svg/window-3.svg"),
            },
            {
              elemSubtitle: "Цветные ручки",
              elemSubtext:
                "Оригинальные оконные ручки подчеркнут дизайн окна. Подберем оптимальный цвет ручек в зависимости от цвета всей конструкции. ",
              elemIcon: require("../../../public/svg/window-4.svg"),
            },
            {
              elemSubtitle: "Проветриватели",
              elemSubtext:
                "Постоянное обновление воздуха в комнате снижает риск аллергии, улучшает сон и благоприятно влияет на самочувствие. ",
              elemIcon: require("../../../public/svg/window-5.svg"),
            },
            {
              elemSubtitle: "Москитные сетки",
              elemSubtext:
                "Нежеланные насекомые останутся на улице, а ваша кошка - в квартире. Устанавливаем сетки для пластиковых окон любых форм и размеров.",
              elemIcon: require("../../../public/svg/window-6.svg"),
            },
          ],
        },
        {
          subtitle: "Остекление балконов и лоджий",
          subtext:
            "Занимаемся остеклением и отделкой балконов и лоджий. Теплое и холодное остекление, изготовление выносов и крыш. Беремся за сложные объекты",
          icon: require("../../../public/svg/service-2.svg"),
          image: require("../../../public/img/service-2.webp"),
          modalTitle: "Остекление балконов и лоджий",
          modalText:
            "Занимаемся остеклением и отделкой балконов и лоджий. Теплое и холодное остекление, изготовление выносов и крыш. Беремся за сложные объекты",
          modalImage: require("../../../public/img/slide-2.webp"),
          modalElems: [
            {
              elemSubtitle: "Тёплое остекление",
              elemSubtext:
                "Теплое остекление — возможность сделать из балкона или лоджии полноценное жилое помещение.",
              elemIcon: require("../../../public/svg/window-1.svg"),
            },
            {
              elemSubtitle: "Холодное остекление",
              elemSubtext:
                "Холодное остекление рекомендовано в случаях, когда балкон или лоджия используются для хранения вещей.",
              elemIcon: require("../../../public/svg/window-2.svg"),
            },
            {
              elemSubtitle: "Панорамное остекление",
              elemSubtext:
                "Остекление от пола до потолка, дающее максимальное естественное освещение и прекрасный обзор окрестностей.",
              elemIcon: require("../../../public/svg/window-3.svg"),
            },
            {
              elemSubtitle: "Остекление с выносом",
              elemSubtext:
                "Способ увеличения площади и объема балкона или лоджии.",
              elemIcon: require("../../../public/svg/window-4.svg"),
            },
            {
              elemSubtitle: "Остекление с крышей",
              elemSubtext:
                "Строительство крыши для домов с высоким потолком и квартир, расположенных на последних этажах.",
              elemIcon: require("../../../public/svg/window-5.svg"),
            },
            {
              elemSubtitle: "Объединение с комнатой",
              elemSubtext:
                "Перепланировка квартиры, дающая дополнительные метры полезной площади и улучшающая жилищные условия.",
              elemIcon: require("../../../public/svg/window-6.svg"),
            },
          ],
        },
        {
          subtitle: "Остекление коттеджей и дач",
          subtext:
            "Остекление и отделка под ключ: от коттеджей и дач до террас и беседок. Выделяем личного технолога под каждый объект",
          icon: require("../../../public/svg/service-3.svg"),
          image: require("../../../public/img/service-3.webp"),
          modalTitle: "Остекление коттеджей и дач",
          modalText:
            "Остекление и отделка под ключ: от коттеджей и дач до террас и беседок. Выделяем личного технолога под каждый объект.",
          modalImage: require("../../../public/img/slide-3.webp"),
          modalElems: [
            {
              elemSubtitle: "Цветные окна",
              elemSubtext:
                "Использование ламинационных окон, ламинации в массе, 3д-ламинации, а также покраска окон.",
              elemIcon: require("../../../public/svg/window-1.svg"),
            },
            {
              elemSubtitle: "Фигурные окна",
              elemSubtext:
                "Арочные окна, окна трапеции, треугольные окна, круглые и многоугольные окна",
              elemIcon: require("../../../public/svg/window-2.svg"),
            },
            {
              elemSubtitle: "Алюминиевые конструкции",
              elemSubtext:
                "Идеальный вариант для большой площади остекления: зимние сады, террасы и т.п..",
              elemIcon: require("../../../public/svg/window-4.svg"),
            },
            {
              elemSubtitle: "Деревянные окна",
              elemSubtext:
                "Экологичное и натуральное решение для остекления любого объекта.",
              elemIcon: require("../../../public/svg/window-3.svg"),
            },
            {
              elemSubtitle: "Портальные решения",
              elemSubtext:
                "Эксклюзивные дверные и балконные раздвижные конструкции для элитных квартир и респектабельных домов, обеспечивающие панорамный вид и экономящие пространство.",
              elemIcon: require("../../../public/svg/window-5.svg"),
            },
            {
              elemSubtitle: "Рольставни и ворота",
              elemSubtext:
                "Защитные рольставни для частных домов, роллетные ворота",
              elemIcon: require("../../../public/svg/window-6.svg"),
            },
          ],
        },
        {
          subtitle: "Остекление корпоративных объектов ",
          subtext:
            "Реализуем сложные проекты по остеклению торговых центров, ресторанов, производственных помещений и офисов",
          icon: require("../../../public/svg/service-4.svg"),
          image: require("../../../public/img/service-4.webp"),
          modalTitle: "Остекление корпоративных объектов",
          modalText:
            "Реализуем сложные проекты по остеклению торговых центров, ресторанов, производственных помещений и офисов",
          modalImage: require("../../../public/img/slide-4.webp"),
          modalElems: [
            {
              elemSubtitle: "Многоквартирные дома",
              elemSubtext:
                "Изготовление и монтаж окон ПВХ под ключ. Приглашаем к партнерству застройщиков",
              elemIcon: require("../../../public/svg/window-1.svg"),
            },
            {
              elemSubtitle: "Офисные помещения",
              elemSubtext:
                "Установка пластиковых окон, офисных перегородок и дверей и входных групп.",
              elemIcon: require("../../../public/svg/window-3.svg"),
            },
            {
              elemSubtitle: "Социальные объекты",
              elemSubtext:
                "Остекляем детские сады, школы, медицинские учреждения",
              elemIcon: require("../../../public/svg/window-2.svg"),
            },
            {
              elemSubtitle: "Объекты торговли",
              elemSubtext:
                "Способ увеличения площади и объема балкона или лоджии.",
              elemIcon: require("../../../public/svg/window-4.svg"),
            },
            {
              elemSubtitle: "Спортивные объекты",
              elemSubtext:
                "Остекляем спортивные залы, бассейны, крытые спорткомплексы",
              elemIcon: require("../../../public/svg/window-5.svg"),
            },
            {
              elemSubtitle: "Производственные помещения",
              elemSubtext:
                "Устанавливаем окна для складских и промышленных зданий в соответствии с требованиями бизнеса",
              elemIcon: require("../../../public/svg/window-6.svg"),
            },
          ],
        },
      ],
    };
  },
  components: { AppService },
};
</script>
