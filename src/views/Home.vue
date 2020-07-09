<template>
  <div class="home">
    <div class="empty-panel"></div>
    <ContentPanel />
    <UserPanel />
  </div>
</template>

<script>
import UserPanel from "@/components/UserPanel.vue";
import ContentPanel from "@/components/ContentPanel.vue";

export default {
  name: "Home",
  components: {
    UserPanel,
    ContentPanel
  }
};
</script>

<style>
.home {
  display: flex;
  flex-direction: column-reverse;
}

.empty-panel {
  display: none;
}

@media (min-width: 600px) {
  .home {
    display: flex;
    flex-direction: row-reverse;
  }

  .user-panel {
    width: 20%;
    height: 100%;
    position: fixed;
    left: 0;
    top: 0;
  }

  .content-panel {
    width: 80%;
  }
}

@media (min-width: 800px) {
  .content-panel {
    width: 60%;
    max-width: 800px;
  }

  .empty-panel {
    display: block;
    width: 20%;
  }
}
</style>
