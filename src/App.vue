<template>
  <v-app :dark="goDark">
    <v-content>
      <v-container align-center>
        <TheHeader :goDark="goDark" @changeTheme="updateTheme($event)"/>

        <transition
          name="router-animation"
          mode="out-in"
          enter-active-class="animated fadeIn fast"
          leave-active-class="animated fadeOut faster"
        >
          <router-view></router-view>
        </transition>
      </v-container>
    </v-content>
    <TheFooter/>
  </v-app>
</template>

<script>
import TheHeader from './components/TheHeader'
import TheFooter from './components/TheFooter'

export default {
  name: 'App',
  metaInfo: {
    title: 'Home',
    titleTemplate: "%s ← Hai Tam Ma",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { name: 'description', content: "Hai Tam Ma Portfolio" },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Hai Tam Ma" },
      { property: 'og:site_name', content: "Hai Tam Ma" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://vuejs.kaydenma.com' },
      {
        property: 'og:image',
        content: 'https://i.imgur.com/7DML0OH.jpg'
      },
      { property: 'og:description', content: "Hai Tam Ma Portfolio" }
    ]
  },
  components: {
    TheHeader,
    TheFooter
  },
  data () {
    return { goDark: true }
  },
  methods: {
    updateTheme (updatedTheme) {
      this.goDark = !updatedTheme
    }
  }
}
</script>
<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.min.css";
</style>
