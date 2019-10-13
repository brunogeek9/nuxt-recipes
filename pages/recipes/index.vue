<template>
  <v-container class="grey lighten-5">
    <v-row no-gutters>
      <Recipe
        thumbnail="https://media-cdn.tripadvisor.com/media/photo-s/0b/10/e1/16/restaurante-refeicao.jpg"
        title="awesome"
        previewText="good"
        id="1"
      />

      <Recipe
        thumbnail="https://media-cdn.tripadvisor.com/media/photo-s/0e/cd/15/90/brasilianorestaurante.jpg"
        title="awesome"
        previewText="good"
        id="2"
      />
    </v-row>
  </v-container>
</template>
<script>
import Recipe from "@/components/Recipe";
export default {
    components:{
        Recipe
    }
};
</script>