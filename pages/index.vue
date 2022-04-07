<template>
    <v-col>
      <h1>2D Array Viewer</h1>
      <ArrayField></ArrayField>
    </v-col>
</template>

<script>
import ArrayField from "../components/ArrayField";
export default {
  name: 'IndexPage',
  components: {ArrayField},
}
</script>
