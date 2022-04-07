<template>
  <v-container>
    <v-card class="mt-8 pa-4">
      <v-row
        class="mb-4">
        <h3>Width:</h3>
        <v-text-field
          v-model.number="x"
          type="number"
          :rules="[sizeRule]"
          dense
        />
        <h3 class="ml-16">Height:</h3>
        <v-text-field
          v-model.number="y"
          type="number"
          dense
        />
      </v-row>
      <div v-if="y <= 50 && x <= 50">
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
              <v-card-text>[{{ j - 1 }}, {{ i - 1 }}]</v-card-text>
              <v-text-field
                value="0"
                class="number"
                type="number"
                justify="center"
              />
            </v-card>
          </v-col>
        </v-row>
      </div>
    </v-card>
  </v-container>
</template>

<script lang="ts">
import {InputValidationRule} from "vuetify";

interface Data {
  x: number
  y: number
}

export default {
  name: 'ArrayCard',
  data(): Data {
    return {
      y: 3,
      x: 10,
    }
  },
  computed: {
    sizeRule(): InputValidationRule {
      return (num: number) => {
        return (num <= 100)
      }
    }
  }
}
</script>

<style>
input {
  font-size: 1.5em;
  text-align: center
}

</style>
