<template>
  <div>
		<v-bottom-navigation
        background-color="indigo darken-1"
        bottom
        fixed
        dark
        app
      >
        <v-btn @click="$router.push({ name: 'dashboard' })">
          <v-icon>mdi-home-outline</v-icon>
        </v-btn>

				<v-btn @click="$router.push({ name: 'messages' })">
          <v-icon>mdi-email-outline</v-icon>
        </v-btn>

        <v-btn @click="sheet = !sheet">
          <v-icon>mdi-plus</v-icon>
        </v-btn>

        <v-btn @click="$router.push({ name: 'profile' })">
          <v-icon>mdi-account-outline</v-icon>
        </v-btn>

				<v-btn @click="$router.push({ name: 'notifications' })">
          <v-icon>mdi-bell-outline</v-icon>
        </v-btn>
      </v-bottom-navigation>

      <v-bottom-sheet v-model="sheet">
        <v-sheet class="text-center" height="300px">
          <v-row>
            <v-col>
              <div class="subtitle-1">
                Create New
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col
              justify="center"
              align="center"
              v-for="item in items"
              :key="item.title"
              cols="4"
            >
              <v-btn outlined fab large>
                <v-icon>{{ item.icon }}</v-icon>
              </v-btn>
              <div class="subtitle-2">
                {{ item.title }}
              </div>
            </v-col>
          </v-row>
        </v-sheet>
      </v-bottom-sheet>
	</div>
</template>

<script>
export default {
  data: () => ({
    sheet: false,
    items: [
      {
        title: 'Cars',
        icon: 'mdi-car'
      },
      {
        title: 'Jobs',
        icon: 'mdi-briefcase',
      },
      {
        title: 'Real Estate',
        icon: 'mdi-domain'
      },
      {
        title: 'Sale',
        icon: 'mdi-currency-usd'
      },
      {
        title: 'Rooms',
        icon: 'mdi-bed-empty'
      },
      {
        title: 'Anything',
        icon: 'mdi-star'
      }
    ],
  }),
}
</script>
