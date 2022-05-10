<template>
  <div class="footer">
    <div class="title">FT_TRANSCENDENCE</div>
    <div class="up-footer">
      <img class="logo-frame" src="../assets/Icon42/nestjs.svg" alt="" />
      <img class="logo-frame" src="../assets/Icon42/nuxt.svg" alt="" />
      <img class="logo-frame" src="../assets/Icon42/postgresql.svg" alt="" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped>
.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 10rem; /* Height of the footer */
  background: #6cf;
  background: #000;
  margin-top: 20px;
  /* padding-top: 50px; */
}
.logo-frame {
  width: 1.5rem;
  height: 1.5rem;
  /* overflow: visible; */
  /* height: 4rem; */
  /* border: 2px solid #6cf; */
  margin-inline: 0.5rem;
  cursor: pointer;
}
p {
  font-family: "Press Start 2P", cursive;
  color: #fff;
  font-weight: 300;
  font-size: 14px;
}
.title {
  padding-top: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: "Press Start 2P", cursive;
  color: #fff;
}
.up-footer {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: row;
}
</style>
