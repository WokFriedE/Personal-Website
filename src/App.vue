<template>
  <span>
    <profileMainVue />
    <projectsVue />

    <div style="border-bottom: 2px solid rgba(0, 0, 0, 0.2); max-width: 75%; margin-inline: 10%;" />
    <br />

    <!-- The languages and skills segment -->
    <div style="display: flex; align-items:center; justify-content: center;">
      <section style="width:50%;">
        <boxListingsVue v-bind:propsdata="languages" />
      </section>
      <section style="width:50%">
        <boxListingsVue v-bind:propsdata="skills" />
      </section>
    </div>

    <!-- The classes segment -->
    <boxListingsVue v-bind:propsdata="classes" style="margin-inline: 4rem;" />

    <div style="border-bottom: 2px solid rgba(0, 0, 0, 0.2); max-width: 75%; margin-inline: 10%;" />
    <br />

    <CardItemVue v-if="false" />

    <!-- The footer segment -->
    <div style="height: 2rem;  background: linear-gradient(0deg, dimgrey 20%, rgba(255, 255, 255,0) 60%); " />
    <footerVue />
  </span>
</template>

<script>
import profileMainVue from "./components/Profile-Main.vue";
import projectsVue from "./components/Projects-Main.vue";
import boxListingsVue from "./components/Box-Listings.vue";
import footerVue from "./components/Footer-Main.vue";
import CardItemVue from "./components/Card-Item.vue";

import skills from "./data/skills.json";
import languages from "./data/languages.json";
import classes from "./data/classes.json";

export default {
  components: {
    profileMainVue,
    projectsVue,
    boxListingsVue,
    footerVue,
    CardItemVue
  },

  data() {
    return {
      skills: skills,
      classes: classes,
      languages: languages
    };
  },
};

//add scroll open effect
</script>

<style>
body {
  background-color: rgb(177, 177, 177);
  margin: 0%;
}
</style>

