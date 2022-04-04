<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title>2D Array Viewer</v-card-title>
      </v-card>
      <ArrayField></ArrayField>
    </v-col>
  </v-row>
</template>

<script>
import ArrayField from "../components/ArrayField";
export default {
  name: 'IndexPage',
  components: {ArrayField},
}
</script>
