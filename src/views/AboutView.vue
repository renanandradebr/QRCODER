<template>
  <v-app>
    <v-main>
      <v-container fluid>
        <v-row justify="center" align="center" class="fill-height">
          <v-col cols="12" sm="8" md="4">
            <v-card>
              <v-card-title class="text-center">
                <h2>LOGIN - QrCode</h2>
              </v-card-title>
              <v-card-text>
                <v-form @submit.prevent="login">
                  <v-text-field
                    v-model="username"
                    label="Nome de Usuário"
                    outlined
                    required
                  ></v-text-field>
                  <v-text-field
                    v-model="password"
                    label="Senha"
                    type="password"
                    outlined
                    required
                  ></v-text-field>
                  <v-btn color="primary" type="submit">Entrar</v-btn>
                </v-form>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <v-footer app>
      <v-footer-title>
        © 2023 CAEMA - Companhia de Saneamento Ambiental do Maranhão
      </v-footer-title>
    </v-footer>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      // Implemente sua lógica de login aqui
      console.log("Usuário: ", this.username);
      console.log("Senha: ", this.password);
    },
  },
});
</script>

<style>
.fill-height {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
