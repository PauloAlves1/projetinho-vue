<template>
  <div>
    <b-navbar type="dark" variant="dark">
      <b-navbar-nav>
        <b-nav-item to="/">Home</b-nav-item>
        <b-nav-item-dropdown text="Usuario" right>
          <b-dropdown-item to="/userList">Lista</b-dropdown-item>
          <b-dropdown-item to="/register">Cadastrar</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      msg: "esse é o HEADER",
    };
  },
};
</script>
