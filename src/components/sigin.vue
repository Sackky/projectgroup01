<template>
  <div>
    <h1>Sig In</h1>
    <v-form ref="form" v-model="valid" lazy-validation>
      <v-text-field v-model="mail" label="Email" required></v-text-field>      
      <v-text-field v-model="password" type="password" style="1" label="Password" required></v-text-field>
      <center>
        <v-btn color="info" class="mr-4" @click="page1">SIG IN</v-btn>
        <v-btn color="error" class="mr-4" @click="page3">Forget Password</v-btn>
        <v-btn color="success" class="mr-4" @click="page2">Register</v-btn>
      </center>
    </v-form>
  </div>
</template>

<script>
export default {
  data: () => ({
    mail: "",
    password: "",
  }),
  methods: {
    validate() {
      if (this.mail) {
        let payload = {
          mail: this.mail,
          password: this.password,
        };
        this.$store.dispatch("setItem", payload);
      }
    },
    reset() {
      this.$refs.form.reset();
    },
    page1() {
      this.$store.state.page = 8;
    },
    page2() {
      this.$store.state.page = 2;
    },
    page3() {
      this.$store.state.page = 3;
    },
  },
};
</script>

<style>
</style>