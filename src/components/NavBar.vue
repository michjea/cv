<template>
  <q-header elevated>
    <q-toolbar>
      <q-btn
        flat
        round
        dense
        icon="menu"
        class="q-mr-sm"
        @click="toggleLeftDrawer"
        v-if="isNotMobile"
      />
      <q-toolbar-title> Jeanne Michel </q-toolbar-title>
      <q-space />
      <q-select
        v-model="locale"
        :options="localeOptions"
        dense
        borderless
        label=""
        emit-value
        map-options
        options-dense
        dark
      >
        <template v-slot:option="scope">
          <q-item v-bind="scope.itemProps" clickable>
            <q-item-section>{{ scope.opt.desc }}</q-item-section>
            <q-item-section side>
              <q-icon :name="scope.opt.emoji" />
            </q-item-section>
          </q-item>
        </template>
      </q-select>
    </q-toolbar>
  </q-header>

  <!-- Drawer -->
  <q-drawer v-model="leftDrawerOpen" side="left" overlay bordered :width="220">
    <q-list>
      <q-item>
        <q-btn
          flat
          round
          dense
          icon="close"
          class="q-mr-sm"
          @click="toggleLeftDrawer"
          color="primary"
        />
      </q-item>
      <q-item clickable @click="goToSection('about')">
        <q-item-section>
          <q-item-label>{{ $t("aboutLink") }}</q-item-label>
        </q-item-section>
      </q-item>
      <q-item clickable @click="goToSection('education')">
        <q-item-section>
          <q-item-label>{{ $t("formationLink") }}</q-item-label>
        </q-item-section>
      </q-item>
      <q-item clickable @click="goToSection('experience')">
        <q-item-section>
          <q-item-label>{{ $t("experienceLink") }}</q-item-label>
        </q-item-section>
      </q-item>
      <q-item clickable @click="goToSection('portfolio')">
        <q-item-section>
          <q-item-label>{{ $t("portfolioLink") }}</q-item-label>
        </q-item-section>
      </q-item>
      <q-item clickable @click="goToSection('contact')">
        <q-item-section>
          <q-item-label>{{ $t("contactLink") }}</q-item-label>
        </q-item-section>
      </q-item>
    </q-list>
  </q-drawer>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import { useI18n } from "vue-i18n";

export default defineComponent({
  name: "NavBar",
  methods: {
    goToSection(id: string) {
      const element = document.getElementById(id);
      element;
      if (element) {
        element.scrollIntoView({
          behavior: "smooth",
        });
      }
    },
  },
  setup() {
    const { locale } = useI18n({ useScope: "global" });

    const leftDrawerOpen = ref(false);
    const toggleLeftDrawer = () => {
      leftDrawerOpen.value = !leftDrawerOpen.value;
    };

    return {
      locale,
      localeOptions: [
        { label: "EN 🇬🇧", desc: "English", value: "en-US", emoji: "🇬🇧" },
        { label: "FR 🇫🇷", desc: "Français", value: "fr-FR", emoji: "🇫🇷" },
      ],
      leftDrawerOpen,
      toggleLeftDrawer,
    };
  },
  computed: {
    isNotMobile() {
      return !this.$q.screen.lt.sm;
    },
  },
});
</script>
