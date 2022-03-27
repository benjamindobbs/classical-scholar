<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row no-gutters>
          <v-card width="95%" style="margin:auto" class="py-12" tile flat>
            <v-img src="../images/January-22/sullivan.jpg"></v-img>
          </v-card>
          <div v-for="(qa, index) in this.list.interview" :key="index" cols="6">
            <v-card class="mx-auto my-12" max-width="75%" hover >
              <v-card-title> {{ qa.question }} </v-card-title>
              <v-card-text> {{ qa.response }} </v-card-text>
            </v-card>
          </div>
          <v-card class="mx-auto my-12" max-width="75%" hover>
              <v-card-title> Classical gear </v-card-title>
              <v-card-text> In order to wear hoodies and sweatpants and other things of the like, it must be Classical gear. To get Classical gear you can go to these websites: </v-card-text>
              <v-card-actions style="justify-content:center">
                  <v-btn
                    center
                    right
                    outlined
                    max-width="450"
                    color="Black"
                    href="https://www.google.com/url?q=https%3A%2F%2Fsideline.bsnsports.com%2Fschools%2Fconnecticut%2Fhartford%2Fclassical-magnet-school&sa=D&sntz=1&usg=AFQjCNF7zIr58yFnvIPu6U6tsLelGAaW9g"
                  >
                    <v-card-text style="font-size:.75em"> BSN Sports </v-card-text>
                  </v-btn>
                  <v-btn
                    center
                    right
                    outlined
                    max-width="450"
                    color="Black"
                    href="https://www.google.com/url?q=https%3A%2F%2Fwww.jbprideuniforms.com%2F&sa=D&sntz=1&usg=AFQjCNGiVG8xfPlLSfvPy13Osk1U7JedVA"
                  >
                    <v-card-text style="font-size:.75em"> JB Pride Uniforms </v-card-text>
                  </v-btn>
                </v-card-actions>
                <v-card-text> Ms. Sullivan did bring up making our own Classical gear. She said that if the school invested in a logo printing machine we could essentially largely cut the prices of the gear, reduce the amount of time in between ordering and receiving the item, and personalize the gear for clubs. </v-card-text>
          </v-card>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
import questions from "../static/json/interview.json";
export default {
  layout: "subjectLanding",
  data: () => ({
    list: questions,
  }),
};
</script>