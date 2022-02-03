<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row no-gutters>
          <v-col
            v-for="subjects in this.list.subjects"
            :key="subjects"
            cols="4"
          >
            <v-card class="mx-auto my-12" max-width="75%" hover>
              <v-img :src="subjects.banner" height="100%" width="100%">
                <v-card-title class="subjectHeading" style="font-size:1.5em">{{
                  subjects.name
                }}</v-card-title>
                <v-card-text class="subjectSubheading" style="font-size:1em">{{
                  subjects.blurb
                }}</v-card-text>
                <v-card-actions>
                  <v-btn
                    center
                    right
                    outlined
                    width: 50%
                    color="Black"
                    :to="subjects.path"
                  >
                    <v-text style="font-size:.75em"> {{ subjects.name }} </v-text>
                  </v-btn>
                </v-card-actions>
              </v-img>
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
  layout: "subjectLanding",
  data: () => ({
    list: SLjson,
  }),
};
</script>
