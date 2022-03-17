<template>
 <v-app>
    <v-main>
      <v-container>
        <v-row no-gutters>
          <v-col
            v-for="(images, index) in this.list.images"
            :key="index"
            cols="4"
          >
          <v-card  class="mx-auto my-12" max-width="75%" hover>
            <v-card-title> {{images.description}} </v-card-title>
            <v-img :src="images.path"></v-img>
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