<template>
      <v-container class="fill-height">
        <v-row justify="center" align="center">
          <v-col cols="12" sm="8" md="6">
            <v-card class="elevation-12">
              <v-btn class="botaologin" type="submit" color="blue" text-color="white" block>Sair</v-btn>
            </v-card>
            <v-card class="elevation-12">
              <v-card-title class="title">
                <h2>Verifique seus Dados</h2>
              </v-card-title>
              <v-card-text>
                <v-form @submit.prevent="submitForm">
                  <v-text-field v-model="matricula" label="Matrícula" required></v-text-field>
                  <v-text-field v-model="nome" label="Nome" required></v-text-field>
                  <v-text-field v-model="setor" label="Setor" required></v-text-field>
                  <v-text-field v-model="cpf" label="CPF" required></v-text-field>
                  <v-file-input v-model="imagem" label="Upload de Imagem"></v-file-input>
                  <v-textarea v-model="observacoes" label="Observações"></v-textarea>
                  <v-btn color="primary" type="submit">Gerar QrCode</v-btn>
                </v-form>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
</template>

<script>
export default {
  data() {
    return {
      matricula: '',
      nome: '',
      setor: '',
      cpf: '',
      imagem: null,
    }; 
  },
  methods: {
    submitForm() {
      // Implemente aqui a lógica para enviar os dados
      console.log('Matrícula:', this.matricula);
      console.log('Nome:', this.nome);
      console.log('Setor:', this.setor);
      console.log('CPF:', this.cpf);
      console.log('Imagem:', this.imagem);
    },
  },
};
</script>

<style>
.fill-height {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title {
  text-align: center;
  border: red 2px;
}
</style>
