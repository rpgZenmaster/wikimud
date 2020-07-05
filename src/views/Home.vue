<template>
  <div class="home">
    <Splash msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import Splash from "@/components/Splash.vue";

export default {
  name: "Home",
  components: {
    Splash
  }
};
</script>
