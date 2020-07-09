<template>
  <div class="user-panel">
    <div v-if="0">You are logged in</div>
    <div v-else>
      <p>
        You are not logged in
      </p>
      <p>
        Would you like to log in?
      </p>
      <form @submit="handleSubmit()">
        <label for="username">Username (min. length 3)</label>
        <br />
        <input type="text" name="username" v-model="form.username" required />
        <br />
        <label for="password">Password (min. length 6)</label>
        <br />
        <input type="password" name="password" v-model="form.password" />
        <br />
        <input type="submit" :disabled="isFormIncomplete" />
      </form>
    </div>
    <router-link to="About">About</router-link>
  </div>
</template>

<script>
export default {
  name: "UserPanel",
  data: function() {
    return {
      form: {
        username: "",
        password: ""
      }
    };
  },
  computed: {
    isFormIncomplete: function() {
      return this.form.username.length < 3 || this.form.password.length < 6;
    }
  },
  methods: {
    handleSubmit() {
      alert("test alert");
    }
  }
};
</script>

<style>
.user-panel a {
  font-weight: bold;
  color: #2c3e50;
}

.user-panel a.router-link-exact-active {
  color: #42b983;
}
</style>
