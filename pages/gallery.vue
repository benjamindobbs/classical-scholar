<template>
 <v-app>
    <v-main>
      <v-container>
        <v-row no-gutters>
          <v-col
            cols="12"
          >
          <v-card v-for="(images, index) in this.list.images" :key="index" width="95%" style="margin:auto" class="py-12"  flat>
          <v-card-title>{{images.description}} </v-card-title>
          <v-img contain :src="images.path"></v-img>
          <v-card-text> {{images.byline}} </v-card-text>
          </v-card>
          </v-col>
        </v-row>
      </v-container>
  </v-main>
</v-app>
</template>
<script>
import Galjson from '../static/json/gallery.json'
export default {
  layout: "subjectLanding",
    data: () => ({
      list: Galjson

    })}

</script>