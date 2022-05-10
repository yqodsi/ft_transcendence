<!-- Please remove this file from your project -->
<template>
  <div class="link-list">
    <a href="" class="logo link"></a>
    <a href="" class="link"><Icon42 /></a>
  </div>
</template>

<script>
import Icon42 from "./Icon42.vue";
export default {
  components: { Icon42 },
  name: "Navbar",
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Lexend:wght@100;200;300;400;500;600;700;800;900&display=swap");
.link-list {
  padding-top: 20px;
  padding-inline: 20px;
  display: flex;
  justify-content: space-between;
}
.link {
  font-weight: 600;
}
.logo {
  background: #292a34;
  border-radius: 100px;
  font-weight: 900;
  width: 40px;
  aspect-ratio: 1;
}
a,
a:hover,
a:focus,
a:active {
  text-decoration: none;
  color: inherit;
}
</style>
