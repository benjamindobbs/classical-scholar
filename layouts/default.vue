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
          v-for="(link, index) in links"
          :key="index"
          :to="link.path"
        >
          {{ link.name }}
          
        </v-tab>
      </v-tabs>
    </v-app-bar>
  </v-app>
</template>

<script>
export default {
    data: () => ({
      links: [
        {name:'Home', path: '/'},
        {name:'Current Issue', path:'/current'},
        {name:'Submit Here', path:'/submissions'},
        {name:'Contributors', path:'/contributors'}
        // {name:'The Archives', path: '/archives'},
        // {name:'About', path: '/about'},
        // {name:'Contributors', path: '/contributers'},
        // {name:'Updates', path: '/updates'},
      ],
    }),
  }
</script>
