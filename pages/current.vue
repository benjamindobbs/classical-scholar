<template>
  <v-app>
    <v-main>
      <v-container fluid>
        <v-row dense>
          <v-col 
          v-for="(subjects, index) in this.list.content"
            :key="index"
            :cols="subjects.flex"
            wrap
            >
            <v-card class="mx-auto my-12" max-width="75%" hover 
            v-for="(items, itemIndex) in subjects.items"
            :key="itemIndex"
            >
              <!-- <v-img :src="items.banner" height="100%" width="100%"> -->
                <v-card-title class="subjectHeading" style="font-size:1.5em">{{
                  items.name
                }}</v-card-title>
                <v-card-text class="subjectSubheading" style="font-size:1em">{{
                  items.blurb
                }}</v-card-text>
                <v-card-actions>
                  <v-btn
                    center
                    right
                    outlined
                    color="Black"
                    large
                    :to="items.path"
                  >
                  <p class="text-wrap" style="width: 65%; margin: auto; font-size:.75em;"> <strong>
                    {{ items.description }} 
                  </strong></p>
                  </v-btn>
                </v-card-actions>
              <!-- </v-img> -->
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
import SLjson from "../static/json/subjectlist.json";
export default {
  data: () => ({
    list: SLjson,
  }),
  layout: "subjectLanding",
};
</script>
