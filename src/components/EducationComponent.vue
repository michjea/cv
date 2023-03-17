<template>
  <div class="row">
    <div class="col-12">
      <q-timeline :layout="layout">
        <q-timeline-entry
          :title="$t('bachelor')"
          subtitle="2020 - 2023"
          color="primary"
          icon="school"
          side="left"
        >
          <div>
            <p>HE-Arc Ingénierie, Neuchâtel, CH</p>
          </div>
        </q-timeline-entry>
        <q-timeline-entry
          :title="$t('matu')"
          subtitle="2019 - 2020"
          color="primary"
          icon="school"
          side="left"
        >
          <div>
            <p>{{ $t("cfcSchool") }}, Porrentruy, CH</p>
          </div>
        </q-timeline-entry>
        <q-timeline-entry
          :title="$t('cfc')"
          subtitle="2016 - 2019"
          color="primary"
          icon="school"
          side="left"
        >
          <div>
            <p>{{ $t("cfcSchool") }}, Porrentruy, CH</p>
          </div>
        </q-timeline-entry>
      </q-timeline>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "EducationComponent",
  setup() {
    return {};
  },
  computed: {
    layout() {
      return this.$q.screen.gt.sm ? "comfortable" : "dense";
    },
  },
});
</script>
