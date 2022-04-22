<template>
  <div class="home">
    <img class="home-img" src="../assets/pong.jpeg" alt="" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HomeView",
  data() {
    return {
      message: "",
      title: "lol" as string,
    };
  },
  components: {},
  methods: {
    changeTitle(name: string) {
      this.title = name;
    },
    changeTitleAgain(name: string) {
      this.changeTitle(name);
    },
  },
  created() {
    document.body.style.backgroundColor = "black";
  },
});
</script>

<style scoped>
.home {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  color: white;
  height: 100vh;
}
.home-img {
  width: 2000px;
  height: auto;
}
</style>
