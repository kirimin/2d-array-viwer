<template>
  <v-container>
    <v-col>
      <h2>要素数</h2>
      <v-row class="mt-8">
        <h3>Height:</h3>
        <v-text-field/>
      </v-row>
      <v-row>
        <h3>Width:</h3>
        <v-text-field/>
      </v-row>
    </v-col>
    <v-row
      v-for="i in 10"
      :key="i"
      :class="i === 1 ? 'mb-6' : ''"
      no-gutters
    >
      <v-col
        v-for="j in 10"
        :key="j"
      >
        <v-card
          outlined
          tile
        >
          <v-text-field />
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<style>
.nuxt-logo {
  height: 180px;
}
</style>
