<template>
  <v-app>
    <v-main>
      <v-container fluid>
        <v-row dense>
          <v-col 
          v-for="subjects in this.list.content"
            :key="subjects"
            :cols="subjects.flex"
            wrap
            >
            <v-card class="mx-auto my-12" max-width="75%" hover 
            v-for="items in subjects.items"
            :key="items"
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
                    :to="items.path"
                  >
                    {{ items.name }} 
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
