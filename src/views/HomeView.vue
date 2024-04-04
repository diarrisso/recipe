<template>
  <RecipeItem 
  :image="recipe.recipe.image"
  :label="recipe.recipe.label"
  :attributes="recipe.recipe.dietLabels.join(',')"
  v-for="recipe in recipes"/>
  
</template>

<script>
import RecipeItem from '@/components/RecipeItem.vue'

  export default {

    components: {
      RecipeItem,
    },

      data() {
        return {
          recipes: []
          
        }
      },


    methods: {
      async getRecipes() {
        const terme = 'sushi';
        const appId = '27bc7b40';
        const appKey = 'cf0ced6efd0de1bdcd58b48345165d9f'
        const url = `https://api.edamam.com/search?q=${terme}&app_id=${appId}&app_key=${appKey}`;
        let resp =  await fetch(url);
        this.recipes = (await resp.json()).hits;

        console.log(this.recipes);


      }

    },

    mounted(){
      this.getRecipes();
    }
  }
</script>
