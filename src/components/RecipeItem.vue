<template>
    <div class="recipe-container">

        <img :src="image"  alt="recette-log" class="recipe-image"/>

        <div class="right-side">
            <div>
                {{ label }}
            </div>

            <div>
                {{ attributes }}
            </div>
        </div>        
        
    </div>
</template>


<script>

    export default {
        name: 'RecipeItem',
        props: {
            image: String,
            label: String,
            attributes: String

        }
    }

</script>



<style scoped>

  .recipe-container {

    border: 1px solid rgba(0,0, 0, 0.2);
    padding: 8px;
    border-radius: 8px;
    margin: 8px;
    display: flex;
    gap: 8px;
  } 

  .recipe-image {

    height: 60px;
  }

  .right-side {
     display: flex;
     flex-direction: column;
  }

</style>