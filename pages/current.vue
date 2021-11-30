<template>
  <v-app>
    <v-main>
      <div v-for="subjects in this.list.subjects" :key="subjects">
        <div>
          <v-parallax :src="subjects.banner" height="200">
            <h1 class="subjectHeading">{{ subjects.name }}</h1>
            <h4 class="subjectSubheading">{{ subjects.blurb }}</h4>
            <v-btn
              center
              right
              outlined
              absolute
              max-width=450
              color="Black"
              :to="subjects.path"
              >
              Go to {{subjects.name}} Catalog
            </v-btn>
          </v-parallax>
        </div>
      </div>
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
