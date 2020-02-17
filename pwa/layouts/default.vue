<template>
  <div>
    <v-app app>
      
      <v-content>
        <v-container>
          <v-row>
            <v-col>
              <nuxt />
            </v-col>
          </v-row>
        </v-container>
      </v-content>
      
      <v-bottom-navigation
        background-color="indigo darken-1"
        bottom
        fixed
        dark
        app
      >
        <v-btn @click="$router.push({ name: 'index' })" value="recent">
          <span>Home</span>
          <v-icon>mdi-home</v-icon>
        </v-btn>

        <v-btn value="favorites">
          <span>New Ad</span>
          <v-icon>mdi-plus</v-icon>
        </v-btn>

        <v-btn value="nearby">
          <span>Profile</span>
          <v-icon>mdi-account</v-icon>
        </v-btn>
      </v-bottom-navigation>
    </v-app>

  </div>
</template>
