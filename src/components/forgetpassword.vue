<template>
  <div>
    <h1>Comfirm Code</h1>
    <v-form ref="form" v-model="valid" lazy-validation>
      <v-text-field v-model="code" label="Code" required></v-text-field>
      <center>
        The security code has been sent to your email. Please check your email.<br>
        <v-btn color="info" class="mr-4" @click="page">Confirm</v-btn>
      </center>
    </v-form>
  </div>
</template>

<script>
export default {
  data: () => ({
    Code: "",
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
      this.$store.state.page = 6;
    },
  },
};
</script>

<style>
</style>