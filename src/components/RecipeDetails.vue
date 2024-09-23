<script>
export default {
  props: {
    recipe: Object
  }
};
</script>

<template>
    <div v-if="recipe">
      <h2>Recipe Details for {{ recipe.name }}</h2>
      <ul>
        <li v-for="ingredient in recipe.ingredients" :key="ingredient.name">
          {{ ingredient.name }} - Cost: ${{ ingredient.cost.toFixed(2) }} - Calories: {{ ingredient.calories }}
        </li>
      </ul>
    </div>
  </template>