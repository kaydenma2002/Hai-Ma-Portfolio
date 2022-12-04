<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Projects</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="project in projects"
        :key="project.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{
                project.title
              }}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="green" text-color="white">{{
              project.tech.tech1
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech2
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech3
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech4
            }}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn
              flat
              large
              dark
              color="green"
              :href="project.git"
              target="_blank"
            >
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>
            <v-btn
              large
              flat
              dark
              color="green"
              :href="project.demo"
              target="_blank"
            >
              <v-icon left>fas fa-desktop</v-icon>Demo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: "Web Portfolio",
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Eldin Zaimovic's Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive",
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Eldin' Space" },
      { property: "og:site_name", content: "Eldin' Space" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://eldin.space" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg",
      },
      {
        property: "og:description",
        content:
          "Eldin Zaimovic's Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive",
      },
    ],
  },
  data() {
    return {
      dialog: false,
      projects: [
        {
          dialog: false,
          title: "Euphoric Voyage",
          git: "https://github.com/EldinZaimovic/euphoric-voyage",
          demo: "https://www.euphoric-voyage.com/",
          tech: {
            tech1: "Gatsby",
            tech2: "JavaScript",
            tech3: "SCSS",
            tech4: "Markdown",
          },
          poster: "https://i.imgur.com/9Ww2bvm.png",
        },
        {
          dialog: false,
          title: "This Site",
          git: "https://github.com/EldinZaimovic/Eldin-Space-Vue",
          demo: "https://eldin.space/",
          tech: {
            tech1: "VUE",
            tech2: "Storyblok",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/MTefNi3.png",
        },
        {
          dialog: false,
          title: "Frontend Developer at Brandly.com",
          git: "https://cdn.neow.in/news/images/uploaded/2018/11/1543476286_cybersecurity.jpg",
          demo: "https://www.brandly.com/",
          tech: {
            tech1: "VUE",
            tech2: "SCSS",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/nVqtTAf.png",
        },
        {
          dialog: false,
          title: "Digital Madness Test",
          git: "https://github.com/EldinZaimovic/Digital-Madness-test",
          demo: "https://digital-madness-test.netlify.com/",
          tech: {
            tech1: "VUE",
            tech2: "CSS",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/GOIIL06.png",
        },
        {
          dialog: false,
          title: "Snowball Coding Challenge",
          git: "https://github.com/EldinZaimovic/SnowBall-Project",
          demo: "https://snowball-test.netlify.com/",
          tech: {
            tech1: "VUE",
            tech2: "GraphQL",
            tech3: "Axios",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/rXHBs36.png",
        },
        {
          dialog: false,
          title: "Snowball Coding Challenge",
          git: "https://github.com/EldinZaimovic/SnowBall-Project",
          demo: "https://snowball-test.netlify.com/",
          tech: {
            tech1: "VUE",
            tech2: "GraphQL",
            tech3: "Axios",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/rXHBs36.png",
        },
      ],
    };
  },
};
</script>

<style  scoped>
</style>
