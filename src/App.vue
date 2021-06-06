<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Vuetify Dashboard</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn>Home</v-btn>
      <v-btn>Login</v-btn>
    </v-app-bar>
    <v-content>
      <!-- Login Module -->
      <v-card width="600" class="mx-auto mt-5">
        <v-card-title>
          <h1 class="display-1">Login</h1>  
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field 
              label="Username"
              prepend-icon="mdi-account-circle"
            ></v-text-field>
            <v-text-field 
              label="Password"
              :type="showPass ? 'text' : 'password' "
              prepend-icon="mdi-lock"
              :append-icon="showPass ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPass = !showPass"
            ></v-text-field>
          </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-action class="d-flex justify-space-between">
          <v-btn color="success">Register</v-btn>
          <v-btn color="info">Login</v-btn>
        </v-card-action>
      </v-card>    
    </v-content>
  </v-app>
</template>
<script>

export default {
  name: 'App',
  components: {
  },

  data: () => ({
    showPass: false
  }),
};
</script>
