<template>
  <div class="navbar">
    <v-container>
      <v-app-bar
        flat
        color="transparent"
        shrink-on-scroll
        prominent
        style="padding-top: 3%"
      >
        <div class="hidden-md-and-down" style="margin: 30px 0 0 0">
          <ul class="d-flex pl-0">
            <li class="bg" v-for="item in menuItems" :key="item.id">
              <nuxt-link :to="item.route"
                ><p class="menuTitles px-3" style="font-size: 18px">
                  {{ item.title }}
                </p></nuxt-link
              >
            </li>
          </ul>
          <!-- <v-btn class="hoverColor" active-class color="white" style="font-size:18px;" text v-for="item in menuItems" :key="item.id">
          {{ item.title }}
        </v-btn> -->
        </div>
        <v-menu bottom left>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              icon
              color="white"
              v-bind="attrs"
              v-on="on"
              class="hidden-lg-and-up pt-8"
            >
              <v-icon>mdi-menu</v-icon>
            </v-btn>
          </template>
          <v-list rounded>
            <v-list-item
              v-for="item in menuItems"
              :key="item.id"
              :to="item.route"
            >
              <v-list-item-content>
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>
        <v-spacer></v-spacer>
        <img
          class="logo"
          src="~/assets/images/General/Navbar/logo.png"
          style="width: 21.187rem; height: 5.625rem"
        />
      </v-app-bar>
      <v-row
        class="d-flex justify-center mt-xl-16 mt-lg-16 mt-md-16 mt-sm-16 pt-10"
      >
        <v-col cols="0" xl="8" lg="8" md="7" sm="6"></v-col>
        <v-col cols="10" xl="4" lg="4" md="5" sm="6" class="float-left">
          <AgahExtractionFarm />
        </v-col>
      </v-row>
      <v-row class="my-10">
        <v-col cols="12" xl="8" lg="8" md="6"></v-col>
        <v-col cols="12" xl="4" lg="4" md="6" class="float-left">
          <BitAndEthRate />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import AgahExtractionFarm from '~/components/General/AgahExtractionFarm.vue'
import BitAndEthRate from '~/components/General/BitAndEthRate.vue'
export default {
  name: 'Navbar',
  components: {
    AgahExtractionFarm,
    BitAndEthRate,
  },
  data() {
    return {
      menuItems: [
        {
          id: 1,
          title: this.$t('menu.homePage'),
          route: '/home',
        },
        {
          id: 2,
          title: this.$t('menu.onlineCalculator'),
          route: '',
        },
        {
          id: 3,
          title: this.$t('menu.minerMachines'),
          route: '',
        },
        {
          id: 5,
          title: this.$t('menu.news'),
          route: '',
        },
        {
          id: 7,
          title: this.$t('menu.aboutUs'),
          route: '',
        },
        {
          id: 8,
          title: this.$t('menu.contact'),
          route: '',
        },
      ],
    }
  },
}
</script>
<style scoped>
.navbar {
  background: url('~assets/images/General/Navbar/slide.jpg');
  background-position-x: center;
  background-position-y: center;
  background-size: cover;
}
@media screen and (max-width: 480px) {
  .logo {
    width: 60vw !important;
  }
}
a {
  color: #fafafa;
}
.bg:hover {
  background-color: #fe8d01;
  border-bottom: 3px solid white;
}
</style>
