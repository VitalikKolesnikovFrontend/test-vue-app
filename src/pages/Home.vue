<script setup>
import AppButton from "@/components/AppButton.vue";
import AppLayout from "@/layouts/AppLayout.vue";
import { RecipeService } from "@/services";
import { onMounted, ref } from "vue";

const recipes = ref();

const fetchRecipes = async () => {
  try {
    recipes.value = await RecipeService.getRecipesByLetter();
  } catch (error) {}
};

onMounted(fetchRecipes);
</script>

<template>
  <AppLayout>
    <template #title>Recipe</template>
    <template #controls>
      <AppButton text="Add recipe" />
    </template>
    <template #inner>{{ recipes }}</template>
  </AppLayout>
</template>
