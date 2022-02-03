<template>
  <v-app>
    <v-main>
      <v-row no-gutters>
        <v-card>
          <v-card-title> January Featured Artist </v-card-title>
          <v-card-subtitle> Josiah Perez-Henry </v-card-subtitle>
          <v-card-text>
            The art of photography itself has been so impactful to my life in
            the past three years and opened up many opportunities for me that
            hadn’t previously been present. But most importantly, it helped me
            decide on what I want to do for a career in the future. It is
            significant to me because it has allowed me to explore myself and
            the world around me in an artistic way. Through my photos, I was
            able to communicate my perspective of the black experience in
            America in a way that felt true and honest to me. A sense of
            identity was found through my lens as the pictures of my imagination
            came into fruition. And the emotions of pain and struggle and
            triumph were chronicled through my Canon Rebel T3.
          </v-card-text>
        </v-card>
        <v-card v-for="images in this.list.images" :key="images" width="100%">
          <v-img :src="images.path"></v-img>
        </v-card>
      </v-row>
    </v-main>
  </v-app>
</template>
<script>
import fa from "../static/json/featuredArtist.json";
export default {
  layout: "subjectLanding",
  data: () => ({
    list: fa,
  }),
};
</script>