<template>
  <div class="user-panel">
    <div v-if="isLogged == True">You are logged in</div>
    <div v-else>
      <p>
        You are not logged in
      </p>
      <p>
        Would you like to log in?
      </p>
      <form>
        <label for="username">Username</label><br />
        <input type="text" name="username"><br />
        <label for="password">Password</label><br />
        <input type="password" name="password"><br />
        <input type="submit" />
      </form>
    </div>
    <router-link to="About">About</router-link>
  </div>
</template>

<script>
export default {
  name: "UserPanel",
  props: {
    isLogged: Boolean
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
