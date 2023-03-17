<template>
  <div class="row justify-center">
    <!-- icon mail with link to mail -->
    <q-btn
      size="xl"
      flat
      round
      dense
      icon="mail"
      class="q-mr-sm"
      @click="openPage('mailto:jeanne.michel@clearcode.ch')"
      color="primary"
    />
    <!-- icon linkedin with link to linkedin -->
    <q-btn
      size="xl"
      flat
      round
      dense
      icon="fa-brands fa-linkedin"
      class="q-mr-sm"
      color="primary"
      @click="openPage('https://www.linkedin.com/in/jeanne-michel')"
    />
    <!-- icon github with link to github -->
    <q-btn
      size="xl"
      flat
      round
      dense
      icon="fa-brands fa-github"
      class="q-mr-sm"
      @click="openPage('https://github.com/michjea')"
      color="primary"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ContactComponent",
  methods: {
    openPage(url: string) {
      window.open(url);
    },
  },
  setup() {
    return {};
  },
});
</script>
