<template>
  <v-container class="grey lighten-5">
    <v-row no-gutters>
      <Recipe
        v-for="recipe in recipes"
        :key="recipe.id"
        :thumbnail="recipe.thumbnail"
        :title="recipe.title"
        :previewText="recipe.previewText"
        :id="recipe.id"
      />

     
    </v-row>
  </v-container>
</template>
<script>
import Recipe from "@/components/Recipe";
export default {
  components: {
    Recipe
  },
  //fake async request
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "almoço com carne",
              thumbnail:
                "https://media-cdn.tripadvisor.com/media/photo-s/0b/10/e1/16/restaurante-refeicao.jpg",
              previewText: "lorem"
            },
            {
              id: "2",
              title: "almoço com frango",
              thumbnail:
                "https://media-cdn.tripadvisor.com/media/photo-s/0b/10/e1/16/restaurante-refeicao.jpg",
              previewText: "lorem"
            }
          ]
        });
      }, 1500);
    });
  }
};
</script>