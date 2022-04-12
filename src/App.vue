<template>
  <div class="app-wrapper">
    <div class="app">
      <navigation />
      <router-view />
    </div>
  </div>
</template>
<script lang="ts">
import Navigation from "@/components/Navigation.vue";
import { defineComponent } from "vue";

export default defineComponent({
  components: {
    Navigation,
  },
  data() {
    return {};
  },
  // created() {},
  // mounted() {},
  methods: {},
  watch: {},
});
</script>
<style lang="scss">
// @import url("https://fonts.googleapis.com/css2?family=Orbitron:wght@600&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700;900&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Lato", sans-serif;
}
.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.container {
  max-width: 1440px;
  margin: 0 auto;
  position: relative;
}
.link {
  cursor: pointer;
  text-decoration: none;
  text-transform: uppercase;
  color: black;
}
.link-light {
  color: #f5f5f5;
}
</style>
