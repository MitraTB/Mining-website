<template>
  <v-container>
    <v-row class="d-flex justify-center my-10">
      <v-col
        cols="12"
        xl="3"
        lg="3"
        md="6"
        sm="6"
        v-for="service in services"
        :key="service.title"
        class="d-flex justify-center"
      >
        <div class="serviceCard d-flex flex-column justify-space-between">
          <div class="d-flex justify-center mt-7">
            <div>
              <img class="icons" :src="service.img" />
            </div>
          </div>
          <h2 style="color: #fe8d01" class="mb-3">
            {{ service.title }}
          </h2>
          <p class="pa-3" style="color: #5b5b5b">{{ service.description }}</p>
          <div class="d-flex justify-center">
            <v-btn tile dark color="#999999">
              {{ $t('inputs.more') }}
            </v-btn>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      services: [
        {
          title: 'ماین اشتراکی بیت کوین',
          description:
            'از طریق ماین اشتراکی شما به اندازه سرمایه خود می توانید به ماین ارز دیجیتال بپردازید. کافی است مقدار سرمایه خود را تعیین کرده تا به همان اندازه قدرت پردازش برایهمیشه به شما تعلق گیرد.',
          img: require('~/assets/images/homePage/services/Group 4198.svg'),
        },
        {
          title: 'مزرعه ماینینگ',
          description:
            'اگر تعداد زیادی ماینر یا سرمایه بالایی دارید و میخواهید در حوزه ماینیگ فعالیت کنید نگران راه اندازی فارم ماینینگ نباشید. فارم روشن ضمیر با تمام امکانات در خدمت ماینرهای شماست.',
          img: require('~/assets/images/homePage/services/Group 3000.svg'),
        },
        {
          title: 'دستگاه ماینر',
          description:
            'در صورتی که میخواهید ماینر بخرید یا ماینر هایی برای فروش دارید می توانید از طریق فروشگاه ماینر روشن ضمیر اقدام به خرید و فروش اواع دستگاه ماینر کنید.',
          img: require('assets/images/homePage/services/Group 4199.svg'),
        },
        {
          title: 'مبادله ارز دیجیتال',
          description:
            'تبدیل ارز دیجیتال به ریال و برعکس گاهی دردسرساز میشود. اکسچنج ارز دیجیتال دیجی تالار به عنوان همکار استراتژیک روشن ضمیر آماده خرید یا فروش ارز',
          img: require('~/assets/images/homePage/services/Group 4200.svg'),
        },
      ],
    }
  },
}
</script>
<style scoped>
.serviceCard {
  background: white;
  text-align: center;
}
.serviceCard:hover {
  transform: translateY(-25px) scale(1.005) translateZ(0);
  box-shadow: 0 24px 36px rgba(0, 0, 0, 0.11);
  border-top: 5px #fe8d01 solid;
}
.v-btn {
  width: 30%;
  transition: width 1s !important;
  margin-bottom: 15px !important;
}
.serviceCard:hover .v-btn {
  background-color: #fe8d01 !important;
  width: 100%;
  margin-bottom: 0 !important;
}
.serviceCard:hover .icons {
  color: #fe8d01;
}
</style>
