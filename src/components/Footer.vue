<template>
	<v-footer
    dark
    padless
		class="mt-6"
  >
    <v-card
      flat
      tile
			color="#102947"
      class="white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon.icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon color="white" size="24px">
						{{icon.icon}}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        O Busca Job é um projeto pessoal, desenvolvido por mim, afim de aperfeiçoar minhas habilidades utilizando o Vue.js, framework
				muito elegante, de fácil aprendizagem e prático. Além disso, também utilizo o Vuetify, que traz animações e componentes ricos
				e simples de se utilizar.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Busca Jobs</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
	name : 'Footer',

	data() {
		return {
			icons : [
				{icon : 'mdi-instagram'},
				{icon : 'mdi-linkedin'},
				{icon : 'mdi-facebook'},
			]
		}
	}
}
</script>

<style>

</style>