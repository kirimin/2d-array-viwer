<template>
  <v-container >
    <v-btn>表をコピー</v-btn>
    <v-card class="mt-8 pa-4">
      <v-row>
        <h3>Width:</h3>
        <v-text-field v-model.number="x"/>
      </v-row>
      <v-row class="mt-8">
        <h3>Height:</h3>
        <v-text-field v-model.number="y"/>
      </v-row>
      <v-row
        v-for="i in y"
        :key="i"
        :class="i === 1 ? 'mb-6' : ''"
        no-gutters
        class="d-flex align-start mb-6"
      >
        <v-col
          v-for="j in x"
          :key="j"
          no-gutters
        >
          <v-card
            outlined
          >
            <v-card-text>({{ j - 1 }}, {{ i - 1 }})</v-card-text>
            <v-text-field
              class="number"
              value="0"
              justify="center"
            />
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script lang="ts">

interface Data {
  x: number
  y: number
}

export default {

  name: 'ArrayField',
  data(): Data {
    return {
      y: 3,
      x: 10,
    }
  },
}
</script>

<style>
.number input {
  font-size: 1.5em;
  text-align: center
}

</style>
