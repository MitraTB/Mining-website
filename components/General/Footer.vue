<template>
  <div>
    <div class="footer">
      <v-container>
        <v-row class="pt-16">
          <v-col cols="12" xl="3" lg="3" md="3" class="mt-5">
            <h2 style="color: #36bfc1" class="pb-5">
              {{ $t('headings.quickAccess') }}
            </h2>
            <div v-for="item in quickMenu" :key="item.title">
              <nuxt-link :to="item.route" style="color: black"
                ><p>{{ item.title }}</p></nuxt-link
              >
            </div>
          </v-col>
          <v-col cols="12" xl="3" lg="3" md="3" class="mt-5">
            <h2 style="color: #36bfc1" class="pb-5">
              {{ $t('headings.services') }}
            </h2>
            <div v-for="item in services" :key="item.title">
              <nuxt-link :to="item.route" style="color: black">
                <p>{{ item.title }}</p></nuxt-link
              >
            </div>
          </v-col>
          <v-col cols="12" xl="2" lg="2" md="1"> </v-col>
          <v-col cols="12" xl="4" lg="4" md="5">
            <img
              src="~/assets/images/General/Navbar/logo.png"
              style="width: 100%"
            />
            <h2 style="color: #ff8a12">{{ $t('headings.newsletters') }}</h2>
            <div class="d-flex">
              <v-text-field
                background-color="#092A44"
                :placeholder="$t('texts.enterEmail')"
                dark
              ></v-text-field>
              <v-btn
                class="mt-4"
                tile
                dark
                color="#FF8A12"
                style="max-height: 32px"
                >{{ $t('inputs.send') }}</v-btn
              >
            </div>
            <div class="d-flex justify-space-between">
              <div style="width: 40%"></div>
              <div>
                <v-btn fab color="#092A44" dark
                  ><v-icon>mdi-instagram</v-icon></v-btn
                >
                <v-btn fab color="#092A44" dark
                  ><v-icon>mdi-linkedin</v-icon></v-btn
                >
                <v-btn fab color="#092A44" dark
                  ><v-icon>mdi-facebook</v-icon></v-btn
                >
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div
      style="
        height: 80px;
        background-color: #082740;
        text-align: center;
        color: #fafafa;
        padding-top: 30px;
      "
    >
      © Copyright 2021. All Rights Reserved.
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      quickMenu: [
        {
          title: this.$t('menu.homePage'),
          route: '/home',
        },
        {
          title: this.$t('menu.news'),
          route: '',
        },
        {
          title: this.$t('menu.articles'),
          route: '',
        },
        {
          title: this.$t('menu.kripto'),
          route: '',
        },
        {
          title: this.$t('menu.education'),
          route: '',
        },
      ],
      services: [
        {
          title: this.$t('services.digitalCurrenctPrices'),
          route: '',
        },
        {
          title: this.$t('services.exchangeOffices'),
          route: '',
        },
        {
          title: this.$t('services.digitalCurrencyCalculator'),
          route: '',
        },
        {
          title: this.$t('services.mining'),
          route: '',
        },
        {
          title: this.$t('services.dictionary'),
          route: '',
        },
      ],
    }
  },
}
</script>
<style scoped>
.footer {
  background: url('~assets/images/General/Footer/bg-footer.jpg');
  background-position: center;
}
p {
  color: #fafafa;
}
</style>
