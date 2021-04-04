<template>
  <v-container>
		<v-row>
			<v-col>
				<v-card class="mt-8" color="#D2BFB8">
					<v-row justify="center">
						<v-col align-self="center" class="mt-8" sm="8" cols="10" lg="8" md="8">
							<v-text-field
								solo
								placeholder="Busque uma oportunidade aqui..."
								prepend-inner-icon="mdi-magnify"
								hint="Professor, desenvolvedor, gerente, etc..."
							></v-text-field>
						</v-col>
						<v-col align-self="center" cols="10" sm="2" lg="2" md="2">
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
  </v-container>
</template>

<script>
export default {

};
</script>

<style>
</style>