<template>
  <div style="margin: 2%">
    <div>
      <router-link to="/AddNewRecipe">
        <v-btn> Add a new recipe </v-btn>
      </router-link>
    </div>
    <br />
    <div class="card-container">
      <div v-for="item in items" :key="item.index">
        <recipe-card class="recipe-card" :Content="item" />
      </div>
    </div>
  </div>
</template>

<script>
import RecipeCard from "../components/RecipeCard.vue";

export default {
  name: "Home",
  components: { RecipeCard },
  data: function () {
    return {
      items: [],
    };
  },

  mounted() {
    var newItems = [];

    for (let i = 0; i < 10; i++) {
      newItems.push({
        Title: "card title",
        Subtitle: "Card subtitle",
        Content: "Some text content",
        Rating: "4.5",
      });
    }

    this.items = newItems;
  },
};
</script>

<style scoped>
.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 20px 20px;
}

.recipe-card {
  flex: 0 1 0;
  min-width: 300px;
  padding: 0;
}
</style>
