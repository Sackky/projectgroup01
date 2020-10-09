<template>
  <div>      
    <h1>Chang Password</h1>
    <v-form ref="form" v-model="valid" lazy-validation>
      <v-text-field v-model="password" type="password" style="1" label="Password" required></v-text-field>
      <v-text-field v-model="password" type="password" style="1" label="Confirm Password" required></v-text-field>
      <center>
        <v-btn color="info" class="mr-4" @click="page">Confirm</v-btn>
      </center>
    </v-form>
  </div>
</template>

<script>
export default {
  data: () => ({
    mail: "",
    numberphone: "",
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
      this.$store.state.page = 7;
    },
  },
};
</script>

<style>
</style>