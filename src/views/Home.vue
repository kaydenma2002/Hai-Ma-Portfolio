<template>
  <v-layout column justify-center align-center class="mt-4 pt-2">
    <img
      v-bind:src="'https://i.imgur.com/7DML0OH.jpg'"
      style="max-width: 15rem; border-radius: 50%"
    />

    <br />

    <vue-typer class="headline" :repeat="0" text="Hai Tam Ma"></vue-typer>
    <vue-typer
      :text="text1"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="erasing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1980"
      :erase-delay="150"
      erase-style="select-back"
      :erase-on-complete="false"
      caret-animation="smooth"
    ></vue-typer>
    <br />
    <v-flex xs12 sm6 md4 lg4 xl4>
      <v-card flat color="transparent" max-width="450">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0 w-100 text-center ">
              <span class="">About Me</span>
            </h3>
            <div>
              <p>
                Hello! I’m Hai Tam Ma. I'm a Full-Stack Web Developer who is
                passionate about
                <span class="green--text font-weight-bold">VUE</span> and
                <span class="red--text font-weight-bold">Laravel</span>.
                Throughout my career, I have contributed to impacting business
                outcomes through effective organization, prioritization, and
                execution of key projects. My skills and qualifications bring
                immediate value to the company's goals. Previously, in my Python
                Web Developer role, I exercised a calculated and methodical
                approach to problem solving. I am independently motivated, yet I
                appreciate team efforts and collaborate productively within
                groups.
              </p>
            </div>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down justify-space-between">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
            
          >
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            small
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from "vue-typer";
import VueCompareImage from "vue-compare-image";

export default {
  metaInfo: {
    title: "Home",
    titleTemplate: "%s ← Hai Tam Ma",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      { name: "description", content: "Hai Tam Ma Portfolio" },
      { charset: "utf-8" },
      { property: "og:title", content: "Hai Tam Ma" },
      { property: "og:site_name", content: "Hai Tam Ma" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://vuejs.kaydenma.com" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg",
      },
      { property: "og:description", content: "Hai Tam Ma Portfolio" },
    ],
  },
  components: {
    "vue-typer": VueTyper,
    VueCompareImage,
  },
  data() {
    return {
      icons: [
        { href: "https://github.com/kaydenma2002", icon: "fab fa-github" },
        {
          href: "https://www.linkedin.com/in/hai-ma-363bb8250/",
          icon: "fab fa-linkedin-in",
        },
       
        {
          href: "https://www.facebook.com/mahaitam2002",
          icon: "fab fa-facebook-f",
        },
        {
          href: "https://www.instagram.com/kaydenma.02/",
          icon: "fab fa-instagram",
        },
      ],
      text1: [
        "PHP Web Developer",
        "Front-End Web Developer",
        "Back-End Web Developer",
      ],

      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5,
    };
  },
};
</script>
<style>
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
.vue-typer .custom.char.typed {
  color: green;
}
.vue-typer .custom.char.selected {
  color: #e91e63;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: green;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>
