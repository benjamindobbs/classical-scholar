<template>
  <v-app light id="inspire">
    <nuxt />
    <v-app-bar app color="grey lighten-3" flat>
      <v-tabs centered class="ml-n9" color="grey darken-1">
        <v-tab to="/current"> Home </v-tab>

        <v-menu v-for="(tabName, index) in this.tabsList.content" :key="index">
          <template v-slot:activator="{ on, attrs }">
            <v-tab v-bind="attrs" v-on="on">
              {{ tabName.name }}
            </v-tab>
          </template>
          <v-list>
            <v-list-item
              v-for="(content, contentIndex) in tabName.items"
              :key="contentIndex"
              :to="content.path"
            >
              <v-list-item-title>{{ content.name }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-tabs>
    </v-app-bar>
  </v-app>
</template>

<script>
import SLjson from "../static/json/subjectlist.json";
export default {
  name: 'TabFormat',
  data: () => ({
    tabsList: SLjson,
  }),
};
</script>
