<template>
  <div class="about">
    <div>
      <ul>
        <li v-for="(book, i) in books" :key="i" :class="{ fav: book.isFav }">
          <h3>{{ book.title }} {{ i }}</h3>
          <p>{{ book.author }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutView",
  data() {
    return {
      showBooks: false,
      books: [
        { title: "name os wind", author: "parick bab", isFav: true },
        { title: "the way of wee", author: "kok mbab", isFav: false },
        { title: "last dance", author: "sheeroke", isFav: true },
      ],
    };
  },
  methods: {},
};
</script>

<style>
.fav {
  background: gold;
}
p,
h3,
ul {
  margin: 0;
  padding: 0;
}
</style>
