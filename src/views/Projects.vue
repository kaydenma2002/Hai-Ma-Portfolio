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
          <v-flex xs12 sm6 md6 lg6 xl6 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="300"
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
    titleTemplate: "%s ??? Hai Tam Ma",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Hai Tam Ma Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive",
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Hai Tam Ma" },
      { property: "og:site_name", content: "Hai Tam Ma" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://vuejs.kaydenma.com" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg",
      },
      {
        property: "og:description",
        content:
          "Hai Tam Ma Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive",
      },
    ],
  },
  data() {
    return {
      dialog: false,
      projects: [
        {
          dialog: false,
          title: "Pay me",
          git: "https://github.com/EldinZaimovic/euphoric-voyage",
          demo: "https://www.euphoric-voyage.com/",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "Javascript",
            tech4: "PHP",
          },
          poster: "https://i.imgur.com/jXKx2B0.png",
        },
        {
          dialog: false,
          title: "Nio Pay",
          git: "https://github.com/EldinZaimovic/Hai-Tam-Ma-Portfolio",
          demo: "http://niopay.io/",
          tech: {
            tech1: "VUE",
            tech2: "Laravel",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/ss9FiY1.png",
        },
        {
          dialog: false,
          title: "This Site",
          git: "https://github.com/EldinZaimovic/Hai-Tam-Ma-Portfolio",
          demo: "https://vuejs.kaydenma.com/",
          tech: {
            tech1: "VUE",
            tech2: "Laravel",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/MTefNi3.png",
        },
        {
          dialog: false,
          title: "Patient dashboard by Laravel",
          git: "https://cdn.neow.in/news/images/uploaded/2018/11/1543476286_cybersecurity.jpg",
          demo: "https://www.brandly.com/",
          tech: {
            tech1: "VUE",
            tech2: "SCSS",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "https://i.imgur.com/izVFoK6.png",
        },

      ],
    };
  },
};
</script>

<style  scoped>
</style>
