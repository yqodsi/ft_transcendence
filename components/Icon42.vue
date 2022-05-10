<template>
  <div class="f-icon">
    <img class="icon" src="../assets/Icon42/42.png" />
    <a style="text-align: center; padding-right: 20px">Login</a>
  </div>
</template>

<script>
export default {
  name: "Icon42",
};
</script>

<style scoped>
.icon {
  width: 40px;
  aspect-ratio: 1;
}
.f-icon {
  display: flex;
  justify-content: space-between;

  align-items: center;
  width: 125px;
  background: white;
  border-radius: 50px;
}
a {
  font-family: "Lexend", sans-serif;
}
</style>
