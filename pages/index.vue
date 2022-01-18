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
          <v-row
          class="pt-15"
          no-gutters 
          align-content="start"
          justify="center"
          >
            <div
            style="text-align:center"
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
            </div>
          </v-row>
          </v-parallax>
        </v-col>
      </v-container>
    </v-main>
</v-app>
</template>
<script>
</script>