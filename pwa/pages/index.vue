<template>
  <div>
    <v-app>
      <v-content>
        <v-container 
          fill-height
          fluid>
          <v-row
              align="center" 
              justify="center"
              class="mx-auto"
          >
            <v-col 
              align="center" 
              justify="center"
              lg="4"
            >
              <div>
                <v-card flat>
                  <v-card-text>
                    <logo />
                    <div class="title">AdApp</div>
                  </v-card-text>
                  <v-card-text>
                    <v-text-field
                      :disabled="signingIn"
                      label="Email"
                      type="email"
                      hide-details
                      class="mb-2"
                      outlined
                      dense
                      flat
                    ></v-text-field>
                    <v-text-field
                      :disabled="signingIn"
                      label="Password"
                      type="password"
                      hide-details
                      class="mb-2"
                      outlined
                      dense
                      flat
                    ></v-text-field>
                  </v-card-text>
                  <v-card-actions class="justify-center">
                    <v-btn 
                      color="indigo darken-1"
                      @click="signIn()"
                      :loading="signingIn"
                      block
                      large
                      dark
                    >
                      <div class="title text-capitalize">
                        Sign In
                      </div>
                      <v-icon right>mdi-arrow-right</v-icon>
                    </v-btn>
                  </v-card-actions>
                  <v-card-actions class="justify-center">
                    <v-btn 
                      color="indigo darken-1"
                      block
                      large
                      dark
                      outlined
                    >
                      <div class="title text-capitalize">
                        Sign Up
                      </div>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-content>
    </v-app>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  layout: 'none',
  
  data: () => ({
    signingIn: false,
  }),
  
  components: {
    Logo
  },

  methods: {
    signIn() {
      setTimeout(() => {
        this.$router.push({ name: 'dashboard' })
      }, 3000)
      this.signingIn = true
      setTimeout(() => {
        this.signingIn = false
      }, 30000)
    },
  }
}
</script>
