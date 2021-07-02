<template>
<v-row>
    <v-col cols="12">
        <VimeoTile video="411777937" ratio="16:9" />
    </v-col>

    <v-col cols="12" class="col-lg-6">
        <VimeoTile video="527689312" ratio="16:9" />
    </v-col>
    <v-col cols="12" class="col-lg-6">
        <VimeoTile video="527688542" ratio="16:9" />
    </v-col>

    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="527685641" ratio="1:1" />
    </v-col>
    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="527687600" ratio="1:1" />
    </v-col>
    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="527701292" ratio="1:1" />
    </v-col>
    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="527708313" ratio="1:1" />
    </v-col>

    <v-col cols="12"  class="col-lg-6">
        <VimeoTile video="367461567" ratio="16:9" />
    </v-col>
    <v-col cols="12"  class="col-lg-6">
        <VimeoTile video="411747911" ratio="16:9" />
    </v-col>

    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="447426337" ratio="4:5" />
    </v-col>
    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="447425498" ratio="4:5" />
    </v-col>
    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="527686278" ratio="4:5" />
    </v-col>
    <v-col cols="12" class="col-md-6 col-lg-3">
        <VimeoTile video="411751543" ratio="4:5" />
    </v-col>
</v-row>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import VimeoTile from "./VimeoTile.vue";

export default defineComponent({
  components: {
    VimeoTile,
  },
  setup() {
    return {};
  },
});
</script>
