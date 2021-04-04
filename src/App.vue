<template>
  <v-app id="back">
    <NavBar></NavBar>
    <v-main>
      <router-view :key="$route.fullPath"></router-view>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar'

export default {
  name: 'App',

  components: {
    NavBar
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
* {
	font-family: 'Montserrat', sans-serif;
}

#back {
  background-color: #F6EFE9;
}
</style>
