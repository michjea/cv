<template>
  <q-page class="row items-center justify-evenly">
    <div class="col-xs-10 col-sm-10 col-md-8 col-lg-6">
      <div id="about">
        <h1>{{ $t("aboutLink") }}</h1>
        <about-component />
      </div>
      <div id="education">
        <h1>{{ $t("titleFormation") }}</h1>
        <education-component />
      </div>
      <div id="experience">
        <h1>{{ $t("titleExperience") }}</h1>
        <experience-component />
      </div>
      <div id="portfolio">
        <h1>Portfolio</h1>
        <portfolio-component />
      </div>
      <div id="contact">
        <h1>Contact</h1>
        <contact-component class="q-pb-xl" />
      </div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import AboutComponent from "components/AboutComponent.vue";
import EducationComponent from "components/EducationComponent.vue";
import ExperienceComponent from "components/ExperienceComponent.vue";
import PortfolioComponent from "components/PortfolioComponent.vue";
import ContactComponent from "components/ContactComponent.vue";

import { useQuasar } from "quasar";

export default defineComponent({
  name: "MainPage",
  components: {
    AboutComponent,
    EducationComponent,
    ExperienceComponent,
    PortfolioComponent,
    ContactComponent,
  },
  setup() {
    const $q = useQuasar();

    return {
      $q,
    };
  },
  mounted() {
    this.$q.notify({
      message: "You are a bêta tester of the new version of my website !",
      color: "warning",
      position: "top",
      timeout: 4000,
    });
  },
});
</script>
