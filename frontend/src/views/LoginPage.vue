<template>
  <v-row
    align="center"
    justify="center"
  >
    <v-card
      class="pa-5"
      width="300"
      max-width="400"
    >
      <v-card-title>
        <v-row
          justify="center"
        >
          <h4>Member Login</h4>
        </v-row>
      </v-card-title>
      <v-container>
        <v-row>
          <v-text-field
            v-model="email"
            label="Email"
          />
        </v-row>
        <v-row>
          <v-text-field
            v-model="password"
            label="Password"
          />
        </v-row>
      </v-container>
      <v-card-actions>
        <v-row
          justify="center"
        >
          <LoginButton
            :email="email"
            :password="password"
            @login="login"
          />
        </v-row>
      </v-card-actions>
    </v-card>
  </v-row>
</template>
<script>
import LoginButton from '@/components/Login/Buttons/LoginButton.vue';

export default {
  components: {
    LoginButton,
  },
  data: () => ({
    email: '',
    password: '',
    isAuthenticated: false,
  }),
  watch: {
    isAuthenticated() {
      if (this.isAuthenticated) {
        this.$router.push('/home');
      }
    },
  },
  methods: {
    login(value) {
      this.isAuthenticated = value;
    },
  },
};
</script>
