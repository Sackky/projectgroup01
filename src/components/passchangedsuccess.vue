<template>
  <div>    
    <v-form ref="form" v-model="valid" lazy-validation>
      <center>
          <h1>Password changed successfully.</h1>
          Please log in again.<br>
        <v-btn color="info" class="mr-4" @click="page">Sig In</v-btn>
      </center>
    </v-form>
  </div>
</template>

<script>
export default {
  data: () => ({
    mail: "",
    numberphone: "",
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
    page() {
      this.$store.state.page = 1;
    },
  },
};
</script>

<style>
</style>