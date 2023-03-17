<template>
  <q-layout view="lHh Lpr lFf">
    <nav-bar />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavBar from "components/NavBar.vue";

export default defineComponent({
  name: "AppLayout",
  components: {
    NavBar,
  },
  setup() {
    return {};
  },
});
</script>
