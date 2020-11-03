<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>
        Edutecno 0049
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text>Home</v-btn>
      <v-btn text>Login</v-btn>
    </v-app-bar>
    <v-content>
      <v-card width="400px" class="my-auto mx-auto">
        <v-card-title>
          <h1>Login</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="Usuario" prepend-icon="mdi-account-circle" />
            <v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Pasword"
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            />
          </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn color="success">Registro</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="info">Login</v-btn>
        </v-card-actions>
      </v-card>
      <v-footer dark padless absolute>
        <v-card class="flex" flat>
          <v-card-title class="primary">
            <strong>Get connected with us on social networks!</strong>
          </v-card-title>
          <v-card-text class="py-2 white--text text-center">
            {{ new Date().getFullYear() }} - <strong>Edutecno</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    showPassword: false,
  }),
};
</script>
