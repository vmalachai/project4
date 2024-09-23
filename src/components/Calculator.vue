<script>
export default {
  props: {
    recipe: Object
  },
  computed: {
    totalCost() {
      return this.recipe.ingredients.reduce((sum, ingredient) => sum + ingredient.cost, 0);
    },
    totalCalories() {
      return this.recipe.ingredients.reduce((sum, ingredient) => sum + ingredient.calories, 0);
    }
  }
};
</script>

<template>
    <div v-if="recipe">
      <h2>Totals for {{ recipe.name }}</h2>
      <p>Total Cost: ${{ totalCost.toFixed(2) }}</p>
      <p>Total Calories: {{ totalCalories }}</p>
    </div>
  </template>