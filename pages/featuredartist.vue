<template>
  <v-app>
    <v-main>
      <v-container grid-list-md >
      <v-row>
        <v-col
          cols="12"
          > 
        <v-card class="mx-auto" tile>
          <v-card-title> January Featured Artist </v-card-title>
          <v-card-subtitle> Josiah Perez-Henry </v-card-subtitle>
          <v-card-text>
            The art of photography itself has been so impactful to my life in
            the past three years and opened up many opportunities for me that
            hadn’t previously been present. But most importantly, it helped me
            decide on what I want to do for a career. It is
            significant to me because it has allowed me to explore myself and
            the world around me in an artistic way. Through my photos, I am
            able to communicate my perspective of the black experience in
            America in a way that felt true and honest to me. A sense of
            identity was found through my lens as the pictures of my imagination
            came into fruition. And the emotions of pain and struggle and
            triumph were chronicled through my Canon Rebel T3.
          </v-card-text>
        </v-card>
        <v-spacer></v-spacer>
        <v-card v-for="(images, index) in this.list.images" :key="index" width="95%" style="margin:auto" class="py-12" tile>
          <v-card-title>{{images.description}} </v-card-title>
          <v-img contain :src="images.path"></v-img>
        </v-card>
        </v-col>
      </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
import fa from "../static/json/featuredArtist.json";
export default {
  data: () => ({
    list: fa,
  }),
  layout: "subjectLanding",
};
</script>