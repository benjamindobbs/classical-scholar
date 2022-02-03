<template>
    <v-app>
        <v-main>
            <v-card>
                <v-card-title> The Battle with Magical Destiny </v-card-title>
                <v-card-subtitle> Charlese Mack <br> Quest Archetype Short Story </v-card-subtitle>
                <v-card-text> {{this.list.shortStory.magicalDestiny}} </v-card-text>
            </v-card>
        </v-main>
    </v-app>
</template>
<script>
import story from "../static/json/shortstory.json";
export default {
  layout: "subjectLanding",
  data: () => ({
    list: story,
  }),
};
</script>