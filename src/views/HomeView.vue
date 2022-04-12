<template>
  <div class="home">
    <h1>This is Home</h1>
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
    document.body.style.backgroundColor = "#041C32";
  },
});
</script>

<style scoped>
.home {
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  height: 100vh;
}
</style>
