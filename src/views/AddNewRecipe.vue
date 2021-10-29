<template>
  <div style="margin:2%" class="add-new-recipe-container">
    <v-btn v-on:click="NavigateBack">Go Back</v-btn>
  </div>
</template>

<script>

export default {
  name: "AddNewRecipe",
  components: {  },
  data: function () {
    return {
      items: [],
    };
  },
  methods: {
      NavigateBack: function() {
        this.$router.go(-1);
      }
  },
  mounted() {
  },
};
</script>

<style scoped>
</style>
