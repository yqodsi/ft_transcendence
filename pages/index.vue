<template>
  <div>
    <Navbar />
    <Home />
    <Footer />
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "IndexPage",
});
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Lexend:wght@100;200;300;400;500;600;700;800;900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap");
body {
  width: 100%;
  height: 100%;
  position: relative;
  min-height: 100%;
  min-height: 100vh;
  background-color: #ded8d2;
  color: #292a34;
}
</style>
