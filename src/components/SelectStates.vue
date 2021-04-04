<template>
	<v-select
		:items="items"
		:placeholder="placeholder"
		solo
		v-model="selectItem"
		item-text="text"
		:hint="hint"
		item-value="value"
	></v-select>
</template>

<script>
export default {
	name: 'SelectStates',

	data() {
		return {
			items = [
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
		}
	}
}
</script>

<style>

</style>