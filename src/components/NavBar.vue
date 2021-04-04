<template>
	<div>
		<v-toolbar
			dark
			color="#102947"
		>
			<v-spacer></v-spacer>
			<v-toolbar-title class="titlePage mt-10">Busca Job</v-toolbar-title>
			<v-spacer></v-spacer>
			<v-btn icon>
				<v-icon>mdi-export</v-icon>
			</v-btn>
			<template v-slot:extension>

			</template>
		</v-toolbar>
		<v-tabs
			v-model="tab"
			align-with-title
			mobile-breakpoint="450"
		>
			<v-tabs-slider color="#D2BFB8"></v-tabs-slider>

			<v-tab class="tabItem" to="/">Achar vagas</v-tab>
			<v-tab class="tabItem" to="/cadastrar-vaga">Cadastrar vagas</v-tab>
		</v-tabs>
	</div>
</template>

<script>
export default {
  name: 'NavBar',

	data() {
		return {
			tab : null
		}
	}
}
</script>

<style scoped>
* {
	font-family: 'Montserrat', sans-serif;
}

.titlePage {
	font-size: 3.5rem !important;
	font-family: 'Montserrat', sans-serif;
	text-align: center;
}

.tabItem {
	font-size: 1rem;
}
</style>