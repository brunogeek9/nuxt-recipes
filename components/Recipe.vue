<template>
  <!-- <nuxt-link :to="'/recipes/'+id"> -->
  <v-col cols="12" sm="4">
    <v-card max-width="400" display="flex" class="mb-5 mr-5">
      <v-img class="white--text align-end" height="200px" :src="thumbnail">
        <v-card-title>{{title}}</v-card-title>
      </v-img>
      <v-card-text class="text--primary">
        <div>{{previewText}}</div>
      </v-card-text>
      <div class="my-2">
        <v-btn large class="ml-2 mb-2" @click="click(id)">Detail</v-btn>
      </div>
    </v-card>
  </v-col>
  <!-- </nuxt-link> -->
</template>
<script>
export default {
  props: ["thumbnail", "title", "previewText", "id"],
  methods: {
    click(where) {
      let path = "/recipes/" + this.id;
      this.$router.push(path);
    }
  },
  
};
</script>
<style scoped>
</style>