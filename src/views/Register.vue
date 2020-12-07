<template>
  <div class="container">
    <b-form @submit="onSubmit">
      <b-form-group
        id="input-group-1"
        label="Email address:"
        label-for="input-1"
        description="We'll never gonna give you up, never gonna let you down... you know the rest"
      >
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          required
          placeholder="E-mail"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          required
          placeholder="Nome"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Sobrenome:" label-for="input-3">
        <b-form-input
          id="input-3"
          v-model="form.lastName"
          required
          placeholder="Sobrenome"
        ></b-form-input>
      </b-form-group>

      <b-button type="submit" variant="primary">Enviar</b-button>
    </b-form>
    <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form }}</pre>
    </b-card>
    <b-table striped hover :items="userList"></b-table>
  </div>
</template>

<script>
export default {
  name: "Register",
  data() {
    return {
      form: {
        email: "",
        name: "",
        lastName: "",
      },
      userList: [
        {
          email: "charmander@hotmail.com",
          name: "charmander",
          lastName: "foguinho",
        },
      ],
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      this.userList.push(this.form);
    },
  },
};
</script>
