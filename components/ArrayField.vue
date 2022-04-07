<template>
  <v-container>
    <ArrayCard/>
<!--    <v-btn class="mb-4">表を複製</v-btn>-->
  </v-container>
</template>

<script lang="ts">

import ArrayCard from "~/components/ArrayCard.vue";

export default {
  name: 'ArrayField',
  components: {ArrayCard},
}
</script>

<style>

</style>
