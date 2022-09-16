<template>
  <v-form v-model="isFormValid" ref="form" @submit.prevent="sendForm">
    <Input label="Correo" :model.sync="email.model" :rules="email.rules" />
    <Input
      label="Contraseña"
      :model.sync="password.model"
      :rules="password.rules"
      :type="password.type"
    />
    <Button :disabled="!isFormValid" label="Ingresar" type="submit" />
  </v-form>
</template>

<script>
export default {
  layout: "login",
  data() {
    return {
      isFormValid: true,
      email: {
        model: "",
        rules: [(v) => !!v || "El correo es requerido"],
      },
      password: {
        model: "",
        rules: [(v) => !!v || "La contraseña es requerida"],
        type: "password",
      },
    };
  },
  methods: {
    sendForm() {
      console.log("email: " + this.email.model);
      console.log("password: " + this.password.model);
      this.$refs.form.reset();
    },
  },
};
</script>

<style></style>
