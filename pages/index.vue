<template>
  <div class="container">
    <div class="tabs-container">
      <div class="tabs-item">
        Nuxt.js
      </div>
      <div class="tabs-item">
        Tutorial
      </div>
      <div class="tabs-item">

      </div>
    </div>
    <!--<Tutorial />-->
    <Component :is="currentTab" />
  </div>
</template>

<script>
import NuxtLogo from "~/components/NuxtLogo.vue";
import Tutorial from "~/components/Tutorial.vue";

const tabNames = {
  NUXT: 'nuxt',
  TUTORIAL: 'tutorial'
};

export default {
  name: "IndexPage",
  data: () => ({
    currentTab: null,
    activeTabName: null
  }),
  components: {
    NuxtLogo,
    Tutorial,
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.tabs-container {
  display: flex;
}

.tabs-item {
  padding: 8px;
  cursor: pointer;
}

.tabs-item:hover {
  background-color: gray;
  color: white;
}
</style>
