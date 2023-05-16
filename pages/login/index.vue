<template>
  <div class="">
    <div class="card-login d-flex justify-center">
      <v-card class="text-center">
        <v-form @submit.prevent>
          <v-text-field
            label="Email"
            variant="solo"
            v-model="email"
            required
          ></v-text-field>

          <v-text-field
            label="Password"
            type="password"
            v-model="password"
            variant="solo"
            required
          ></v-text-field>

          <v-btn type="submit" @click="login" color="primary">Login</v-btn>
        </v-form>
      </v-card>
    </div>
  </div>
</template>
<script lang="ts">
export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    login() {
      console.log("email: " + this.email + "; password: " + this.password);
      this.$router.push("/");
    },
  },
};
</script>
<style lang="scss">
.card-login {
  .v-card {
    width: 40%;
    margin-top: 200px;
    padding: 50px;
  }
}
</style>