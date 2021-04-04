<template>
  <v-container fluid>
		<div v-if="loadingPage">
			<v-progress-linear
				indeterminate
				color="indigo darken-4"
			></v-progress-linear>
		</div>
		<div v-else class="page-content">	
			<v-row justify="center">
				<v-col lg="10" sm="12">
					<v-card class="mt-8" color="#D2BFB8">
						<v-row justify="center">
							<v-col align-self="center" class="mt-8" sm="6" cols="10" lg="5" md="5">
								<v-text-field
									solo
									placeholder="Busque uma oportunidade aqui..."
									prepend-inner-icon="mdi-magnify"
									hint="Professor, desenvolvedor, gerente, etc..."
								></v-text-field>
							</v-col>
							<v-col class="mt-8" cols="10" lg="3" md="3" sm="4">
								<v-select
									:items="items"
									placeholder="Selecione o estado"
									solo
									item-text="text"
									hint="Estado onde deseja trabalhar"
									item-value="value"
								></v-select>
							</v-col>
							<v-col align-self="center" cols="10" sm="10" lg="2" md="2">
								<v-btn
									elevation="2"
									large
									color="#102947"
									dark
								>
									<v-icon
										dark
									>
										mdi-magnify
									</v-icon>				
									Buscar
								</v-btn>
							</v-col>
						</v-row>
					</v-card>
				</v-col>
			</v-row>
			<v-row>
				<v-col>
					<!-- TODO: VAGAS MAIS NOVAS -->
				</v-col>
			</v-row>
		</div>
  </v-container>
</template>

<script>
export default {

	data() {
		return {
			items : [],
			loadingPage : false
		}
	},

	created() {
		this.makeScreen()
	},

	methods : {
		makeScreen() {
			this.loadingPage = true
			this.getStates()
		},

		getStates() {
			this.items = [
				{text : 'Todo Brasil', value : ''},
				{text : 'Acre', value : 'acre'},
				{text : 'Alagoas', value : 'alagoas'},
				{text : 'Amapá', value : 'amapa'},
				{text : 'Amazonas', value : 'amazonas'},
				{text : 'Bahia', value : 'bahia'},
				{text : 'Ceará', value : 'ceara'},
				{text : 'Distrito Federal', value : 'distritofederal'},
				{text : 'Espírito Santo', value : 'espiritosanto'},
				{text : 'Goiás', value : 'goias'},
				{text : 'Maranhão', value : 'maranhao'},
				{text : 'Mato Grosso', value : 'matogrosso'},
				{text : 'Mato Grosso do Sul', value : 'matogrossodosul'},
				{text : 'Minas Gerais', value : 'minasgerais'},
				{text : 'Pará', value : 'para'},
				{text : 'Paraíba', value : 'paraiba'},
				{text : 'Paraná', value : 'parana'},
				{text : 'Pernambuco', value : 'pernambuco'},
				{text : 'Piauí', value : 'piaui'},
				{text : 'Rio de Janeiro', value : 'rj'},
				{text : 'Rio Grande do Norte', value : 'riograndedonorte'},
				{text : 'Rio Grande do Sul', value : 'riograndedosul'},
				{text : 'Rondônia', value : 'rondonia'},
				{text : 'Roraima', value : 'roraima'},
				{text : 'Santa Catarina', value : 'santacatarina'},
				{text : 'São Paulo', value : 'sp'},
				{text : 'Sergipe', value : 'sergipe'},
				{text : 'Tocantins', value : 'tocantins'},
			]
			this.loadingPage = false
		}
	}
};
</script>

<style>
</style>