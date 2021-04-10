<template>
	<v-dialog 
		v-model="showModal"
		max-width="600px"
		transition="dialog-bottom-transition"
	>
		<v-card color="#F6EFE9">
			<v-card-title color="#F6EFE9">
				<v-tabs
          v-model="tabs"
          centered
					name="tabLogin"
          slider-color="#D2BFB8"
					background-color="#F6EFE9"
        >
          <v-tab>
						Login
          </v-tab>
          <v-tab>
						Cadastrar
          </v-tab>
        </v-tabs>
			</v-card-title>
			<v-card-text>
				<v-tabs-items v-model="tabs">
					<v-tab-item class="pt-8" style="background-color: #F6EFE9">
						<v-form ref="loginForm">
							<v-row justify="center">
								<v-col lg="10">
									<v-text-field
										prepend-inner-icon="mdi-account"
										solo delse
										:rules="[rules.required]"
										placeholder="Nome de usuário"
									></v-text-field>
								</v-col>
							</v-row>
							<v-row justify="center">
								<v-col lg="10">
									<v-text-field
										prepend-inner-icon="mdi-lock"
										solo delse
										:type="show1 ? 'text' : 'password'"
										placeholder="Senha"
										:rules="[rules.required]"
										:append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
										@click:append="show1 = !show1"
									></v-text-field>
								</v-col>
							</v-row>
							<v-row justify="center">
								<v-col class="mb-4" lg="10">
									<v-btn
										block
										elevation="2"
										large
										color="#102947"
										dark
										@click="verifyLogin"
									>Acessar</v-btn>
								</v-col>
							</v-row>
							<v-row justify="center">
								<v-col class="mb-4" lg="4">
									<v-btn
										text
										color="#102947"
									>Esqueci a senha</v-btn>
								</v-col>
							</v-row>
						</v-form>
					</v-tab-item>
					<v-tab-item style="background-color: #F6EFE9">
						<v-row>
							<v-col lg="6">
								<v-checkbox
									v-model="typeUser"
									label="Procurar oportunidades"
									value="candidato"
								></v-checkbox>
							</v-col>
							<v-col lg="6">
								<v-checkbox
									v-model="typeUser"
									value="empresa"
									label="Cadastrar vagas"
								></v-checkbox>
							</v-col>
						</v-row>
						<v-row v-if="typeUser == 'candidato'">
							<v-col>
								<v-card>
									<v-card-title>Candidato <v-icon class="pl-2" color="#102947">mdi-account</v-icon></v-card-title>
									<v-card-text>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												label="Nome completo"
												></v-text-field>
											</v-col>
										</v-row>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												label="CPF"
												></v-text-field>
											</v-col>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												type="date"
												label="Data de nascimento"
												></v-text-field>
											</v-col>
										</v-row>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required, rules.emailValid]"
												label="E-mail"
												></v-text-field>
											</v-col>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												label="Confirmação de e-mail"
												></v-text-field>
											</v-col>
										</v-row>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												type="password"
												label="Senha"
												></v-text-field>
											</v-col>
											<v-col>
												<v-text-field
												outlined dense
												type="password"
												:rules="[rules.required]"
												label="Confirmação de senha"
												></v-text-field>
											</v-col>
										</v-row>
									</v-card-text>
								</v-card>
							</v-col>
						</v-row>
						<v-row v-if="typeUser == 'empresa'">
							<v-col>
								<v-card>
									<v-card-title>Anunciante / Empresa <v-icon class="pl-2" color="#102947">mdi-briefcase</v-icon></v-card-title>
									<v-card-text>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												label="Nome completo / Nome empresarial"
												></v-text-field>
											</v-col>
										</v-row>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												label="CNPJ / CPF"
												></v-text-field>
											</v-col>
										</v-row>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required, rules.emailValid]"
												label="E-mail"
												></v-text-field>
											</v-col>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												label="Confirmação de e-mail"
												></v-text-field>
											</v-col>
										</v-row>
										<v-row dense>
											<v-col>
												<v-text-field
												outlined dense
												:rules="[rules.required]"
												type="password"
												label="Senha"
												></v-text-field>
											</v-col>
											<v-col>
												<v-text-field
												outlined dense
												type="password"
												:rules="[rules.required]"
												label="Confirmação de senha"
												></v-text-field>
											</v-col>
										</v-row>
									</v-card-text>
								</v-card>
							</v-col>
						</v-row>
						<v-row v-if="typeUser" justify="center">
							<v-col class="mb-4" lg="12">
								<v-btn
									block
									elevation="2"
									large
									color="#102947"
									dark
								>Cadastrar</v-btn>
							</v-col>
						</v-row>
					</v-tab-item>
				</v-tabs-items>
			</v-card-text>
		</v-card>
	</v-dialog>
</template>

<script>
export default {

	props : ['value'],

	data() {
		return {
			showModal : false,
			tabs : null,
			show1 : false,
			//regra de obrigatório para os campos
			rules: {
				required: value => !!value || 'Campo obrigatório',
				emailValid: value => /.+@.+/.test(value) || 'E-mail deve ser válido',
			},
			typeUser : null
		}
	},

	created() {
		this.showModal = this.value
	},

	methods : {
		verifyLogin() {
			//verifica se o formulário atende todas as regras
			if (this.$refs.loginForm.validate()) {
				//método para chamar autenticação na aplicação
			}
		}
	},

	watch : {
		//verifico se houve mudança no value
		//para que o showModal esteja sempre sincronizado
		value(val) {
			this.showModal = val
		},
		//caso o usuário feche o modal
		//aviso e passo o novo valor ao
		// componente pai utilizando evento
		showModal(val)  {
			if(!val) {
				this.$emit('input', val)
				//limpando o formulário e as mensagens
				this.$refs.loginForm.reset()
			}
		}
	}
}
</script>

<style>

</style>