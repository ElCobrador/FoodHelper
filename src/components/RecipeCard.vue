<template>
  <v-container class="recipe-card-container">
    <v-card class="card" elevation="2">
      <v-card-title>
        {{ Content.Title }}
      </v-card-title>
      <v-card-subtitle>
        {{ Content.Subtitle }}
      </v-card-subtitle>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "RecipeCard",

  props: {
    Content: {
      Title: String,
      Subtitle: String,
      Content: String,
      Rating: Number,
    },
  },
  data: () => ({}),
  mounted() {},
};
</script>

<style scoped>
</style>
