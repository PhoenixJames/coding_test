<template>
  <span>
    <v-btn
      color="primary"
      @click="login"
    >
      Login
    </v-btn>
  </span>
</template>
<script>
export default {
  name: 'LoginButton',
  props: {
    email: {
      type: String,
      default: () => '',
    },
    password: {
      type: String,
      default: () => '',
    },
  },
  data: () => ({
    users: [
      {
        email: 'admin@mail.com',
        password: 'passw0rd',
      },
      {
        email: 'testuser@mail.com',
        password: '12345678',
      },
    ],
  }),
  methods: {
    login() {
      const user = this.users.find((e) => e.email === this.email);
      if (user) {
        if (user.password === this.password) {
          this.$emit('login', true);
        } else {
          this.$emit('login', false);
        }
      } else {
        this.$emit('login', false);
      }
    },
  },
};
</script>
