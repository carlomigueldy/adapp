<template>
  <div>
    <v-app app>
      
      <v-content>
        <nuxt />
      </v-content>
      
      <BottomNavigation />
    </v-app>
  </div>
</template>

<script>
import BottomNavigation from '@/components/BottomNavigation'

export default {
  components: {
    BottomNavigation
  }
}
</script>