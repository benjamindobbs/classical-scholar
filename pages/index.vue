<template>
<v-app light>
    <v-main >
      <v-container
      fill-height
      fluid
      align-items="top"
      >
        <v-col
        no-gutters
        >
          <v-parallax
          src="../parallax.png"
          >
          <v-spacer/>
          <v-row
          class="pt-15"
          no-gutters 
          align="top"
          justify="center"
          >
          <v-col
          class="pt-15"
          align="center"
          justify="center"
          >
          <h1>
            Welcome to the Classical Scholar
          </h1>
          <h3 class="subheading">
            News and Views From Gladiator Nation
            
          </h3>
          <v-btn
              class="ma-2"
              outlined
              color="indigo"
              to="/current"
              >
              Read Our Current Issue
            </v-btn>
            <v-spacer/>
          </v-col>
          </v-row>
          <v-spacer/><v-spacer/> <v-spacer/><v-spacer/>
          </v-parallax>
        </v-col>
      </v-container>
    </v-main>
</v-app>
</template>
<script>
</script>