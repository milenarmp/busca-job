<template>
	<v-container fluid class="mb-5">
		<div v-if="loadingPage">
			<v-progress-linear
				indeterminate
				color="indigo darken-4"
			></v-progress-linear>
		</div>
		<div v-else class="page-content">	
			<v-row>
				<v-col>
					<v-card>
						<v-card-title class="pt-5">Cadastre vagas aqui e tenha acesso à milhões de candidatos</v-card-title>
						<v-card-text>
							<v-row justify="center">
								<v-col align-self="center" cols="12" lg="7"> 
									<p class="fontPropaganda">Os candidatos podem se cadastrar de qualquer canto do país, possibilitando a conexão entre o recrutador e 
									àquele que está em busca de uma nova oportunidade no mercado de trabalho.<br><br><strong> Faça parte dessa rede!</strong></p>
									<v-btn
										elevation="2"
										large
										color="#102947"
										dark
										class="text-capitalize"
									>
										<v-icon class="pr-1">mdi-briefcase-plus-outline</v-icon>
									Cadastrar vagas</v-btn>
								</v-col>
								<v-col cols="12" lg="4">
									<v-img
										lazy-src="/img/mapa.jpg"
										max-height="500"
										max-width="500"
										src="/img/mapa.jpg"
									></v-img>
								</v-col>
							</v-row>
						</v-card-text>
						<v-row>
							<v-col class="text-center" cols="12" lg="12" md="12">
								<p class="fontRecruit">Recrute e selecione de forma eficaz</p>
							</v-col>
						</v-row>
						<v-row>
							<v-spacer></v-spacer>
							<v-col class="text-center" cols="12" md="3" lg="3">
								<p class="fontPropaganda">
									<v-icon color="#102947">mdi-magnify</v-icon>
									Visualização de currículos
								</p>
								<p>Perfis mais completos ganham mais detaque para facilitar a triagem</p>
							</v-col>
							<v-col class="text-center" cols="12" md="3" lg="3">
								<p class="fontPropaganda">
									<v-icon color="#102947">mdi-bullhorn</v-icon>
									Divulgação de vagas
								</p>
								<p>Vagas que podem ser visualizadas por qualquer pessoa do país</p>
							</v-col>
							<v-spacer></v-spacer>
						</v-row>
					</v-card>
				</v-col>
			</v-row>
		</div>
	</v-container>
</template>

<script>
export default {

	data() {
		return {
			loadingPage : false
		}
	}
}
</script>

<style scoped>
.fontPropaganda {
	font-size: 1.25rem !important;
}

.fontRecruit {
	font-size: 2rem !important;
}
</style>