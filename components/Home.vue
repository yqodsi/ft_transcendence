<template>
  <div class="container layout">
    <p>
      Pong was the first commercially successful video game, and it helped to
      establish the video game industry along with the Magnavox Odyssey. Soon
      after its release, several companies began producing games that closely
      mimicked its gameplay.
    </p>
    <img class="pong-img" src="../assets/Pong1.jpeg" alt="" />
    <!-- <nuxt-link to="/lol">click ne</nuxt-link> -->
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
p {
  font-weight: 400;
  color: white;
  padding: 20px;
  border-radius: 5px;
  background: black;
  width: 80%;
  text-align: center;
  font-size: 14px;
  line-height: 2rem;
  font-family: "Press Start 2P", cursive;
}
.pong-img {
  border-radius: 5px;
  width: 80%;
  height: auto;
}
.layout {
  gap: 50px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
  padding-bottom: 30rem;
  padding-top: 100px;
}
</style>
