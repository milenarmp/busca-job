<template>
  <v-app id="back">
    <NavBar></NavBar>
    <v-main>
      <router-view :key="$route.fullPath"></router-view>
    </v-main>
		<Footer></Footer>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar'
import Footer from './components/Footer'

export default {
  name: 'App',

  components: {
    NavBar,
		Footer
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
