<script>
export default {
  props: {
    recipes: Array
  },
  methods: {
    selectRecipe(recipe) {
      this.$emit('recipe-selected', recipe);
    }
  }
};
</script>

<template>
    <div>
      <h2>Select a Recipe</h2>
      <ul>
        <li v-for="recipe in recipes" :key="recipe.name" @click="selectRecipe(recipe)">
          {{ recipe.name }}
        </li>
      </ul>
    </div>
  </template>