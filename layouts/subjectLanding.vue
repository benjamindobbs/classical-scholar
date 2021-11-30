<template>
  <v-app light id="inspire">
    <nuxt />
    <v-app-bar
      app
      color="grey lighten-3"
      flat
    >

      <v-tabs
        centered
        class="ml-n9"
        color="grey darken-1"
        
      >
      <v-tab
      :to="'/'"
      >
      Home
      </v-tab>
        <v-tab
          v-for="subjects in this.list.subjects" 
          :key="subjects"
          :to="subjects.path"
        >
          {{ subjects.name }}
          
        </v-tab>
      </v-tabs>
    </v-app-bar>
  </v-app>
</template>

<script>
import SLjson from '../static/json/subjectlist.json'
export default {
    data: () => ({
      list: SLjson

    })}

</script>
