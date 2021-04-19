<template>
  <v-app :dir="selectedLanguage()">
    <Navbar />
    <v-main>
      <Nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>
<script>
import Navbar from '~/components/General/Navbar.vue'
import Footer from '~/components/General/Footer.vue'
export default {
  components: {
    Navbar,
    Footer,
  },
  methods: {
    selectedLanguage() {
      return this.$i18n.locale === 'en' ? 'ltr' : 'rtl'
    },
  },
}
</script>
