<template>
  <v-app>
    <NavBar />
    <v-content>
      <router-view></router-view>
    </v-content>

  </v-app>
</template>

<script> 
import NavBar from '@/components/NavBar.vue'

  export default ({
    nome: 'App',
    components: {NavBar},
    
  })
</script>

<style scoped>

</style>