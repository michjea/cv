<template>
  <div class="row justify-between">
    <div class="col-md-3 col-sm-12 q-pb-md">
      <q-card>
        <img src="" alt="" />
        <q-card-section>
          <div class="text-h6">{{ $t("fftTitle") }}</div>
        </q-card-section>
        <q-card-section>
          <div>
            <p>{{ $t("fftDescription") }}</p>
            <p>Technologies :Python, OpenCV, NumPy, Matplotlib.</p>
          </div>
        </q-card-section>
      </q-card>
    </div>
    <div class="col-md-3 col-sm-12 q-pb-md">
      <q-card>
        <img src="" alt="" />
        <q-card-section>
          <div class="text-h6">Motarc</div>
        </q-card-section>
        <q-card-section>
          <div>
            <p>{{ $t("motarcDescription") }}</p>
            <p>Technologies : PHP, Laravel, Vue.js, JavaScript, Intertia.js, Quasar.</p>
          </div>
        </q-card-section>
      </q-card>
    </div>
    <div class="col-md-3 col-sm-12">
      <q-card>
        <img src="" alt="" />
        <q-card-section>
          <div class="text-h6">TreeUnroller</div>
        </q-card-section>
        <q-card-section>
          <div>
            <p>
              {{ $t("treeDescription") }}
            </p>
            <p>Technologies : JavaScript, Bootstrap, HTML, CSS.</p>
          </div>
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "PortfolioComponent",
  setup() {
    return {};
  },
});
</script>
