<template>
  <div class="row justify-center">
    <div class="col-md-2 col-sm-12">
      <q-tabs v-model="tab" :vertical="vertical">
        <q-tab name="experience" :label="$t('titleExperience')" />
        <q-tab name="studentjobs" :label="$t('studentJobs')" />
      </q-tabs>
    </div>

    <div class="col-md-10 col-sm-12">
      <q-tab-panels v-model="tab">
        <q-tab-panel name="experience">
          <q-timeline :layout="layout">
            <q-timeline-entry
              :title="$t('experienceMeyer')"
              :subtitle="$t('july') + ' 2022'"
              color="primary"
              icon="work"
              side="left"
            >
              <div>
                <p>{{ $t("meyer") }}, Les Pommerats</p>
                <p>{{ $t("experienceMeyerDescription") }}</p>
                <p>{{ $t("tools") }} : Wordpress, JavaScript, HTML, CSS</p>
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              :title="$t('experienceJAG')"
              :subtitle="$t('november') + ' 2018' + ' - ' + $t('august') + ' 2019'"
              color="primary"
              icon="work"
              side="left"
            >
              <div>
                <p>{{ $t("jag") }}, Porrentruy, CH</p>
                <p>{{ $t("experienceJAGDescription") }}</p>
                <p>
                  {{ $t("tools") }} : C#, TypeScript, JavaScript, Microsoft Visual Studio
                </p>
              </div>
            </q-timeline-entry>
          </q-timeline>
        </q-tab-panel>
        <q-tab-panel name="studentjobs">
          <q-timeline :layout="layout">
            <q-timeline-entry
              :title="$t('manorTitle')"
              :subtitle="$t('may') + ' - ' + $t('december') + ' 2022'"
              color="primary"
              icon="work"
              side="left"
            >
              <div>
                <p>{{ $t("manor") }}, Marin</p>
                <p>{{ $t("manorDescription") }}</p>
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              :title="$t('covidTitle')"
              :subtitle="$t('january') + ' - ' + $t('march') + ' 2022'"
              color="primary"
              icon="work"
              side="left"
            >
              <div>
                <p>{{ $t("covid") }}, Delémont</p>
                <p>
                  {{ $t("covidDescription") }}
                </p>
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              :title="$t('mcdoTitle')"
              :subtitle="$t('september') + ' 2020 - ' + $t('september') + ' 2021'"
              color="primary"
              icon="work"
              side="left"
            >
              <div>
                <p>McDonald's, Delémont</p>
                <p>
                  {{ $t("mcdoDescription") }}
                </p>
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              :title="$t('sontexTitle')"
              :subtitle="$t('july') + ' - ' + $t('august') + ' 2016'"
              color="primary"
              icon="work"
              side="left"
            >
              <div>
                <p>Sontex SA, Sonceboz</p>
                <p>{{ $t("sontexDescription") }}</p>
              </div>
            </q-timeline-entry>
          </q-timeline>
        </q-tab-panel>
      </q-tab-panels>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "ExperienceComponent",
  setup() {
    return {
      tab: ref("experience"),
    };
  },
  computed: {
    vertical() {
      return this.$q.screen.gt.sm;
    },
    layout() {
      return this.$q.screen.gt.sm ? "comfortable" : "dense";
    },
  },
});
</script>
