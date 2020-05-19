<template>
  <div class="developer-card-wrapper">
    <developer-card
      v-for="developer in developers"
      :developerName="developer.name"
      :techStack="developer.techStack"
      :key="developer.id"
      :developerActivity="developer.activity"
      :developerDirection="developer.direction"
      :developerYears="developer.yearsOld"
      :qualification="developer.qualification"
      :special="developer.special"
      :developerHour="developer.bidPerHour"
      :developerEP="developer.dev_ep"
      :developerInn="developer.inn_dev"
      :developerSystem="developer.dev_system"
    ></developer-card>
  </div>
</template>
<script>
import DeveloperCard from "@/components/DeveloperCard.vue";

export default {
  name: "Developers",
  components: {
    DeveloperCard
  },
  data: function() {
    return {
      developers: [
        {
          yearsOld: " 34 года • 11 лет и 9 месяцев опыта работы",
          bidPerHour: "1 100 ₽",
          workExperience: "11 лет и 9 месяцев опыта работы",
          activity: " Frontend",
          direction: " Веб программирование",
          name: "Антон Свирягин",
          special: [
            "Управление проектами",
            "Финтех",
            "Управленчский учет",
            "Финансовое моделирование",
            "Аналитика рынков",
            "Автоматизация рынков",
            "Автоматизация трейдинга",
            "Торговые алгоритмы"
          ],

          qualification: "Lead",
          techStack: [
            "React JS",
            "Redux",
            "Webpack",
            "Redux - Thun",
            "Python 3",
            "Django",
            "AIOHTTP",
            "MongoDB/Postgres",
            "RabbitMQ/Redis",
            "Docker"


          ],
          inn_dev: "492372947",
          dev_ep: " ИП Свирягин Антон Сергеевич",
          dev_system: "УСН",
          id: 1
        }
      ]
    };
  }
};
</script>
