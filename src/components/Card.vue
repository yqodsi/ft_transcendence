<template>
  <div>
    <MDBCard class="w-25">
      <a v-mdb-ripple="{ color: 'light' }">
        <MDBCardImg
          src="https://mdbootstrap.com/img/new/standard/nature/184.webp"
          top
          alt="..."
        />
      </a>
      <MDBCardBody>
        <MDBCardTitle>Card title</MDBCardTitle>
        <MDBCardText>
          Some quick example text to build on the card title and make up the
          bulk of the card's content.
        </MDBCardText>
        <MDBBtn tag="a" href="#!" color="primary">Button</MDBBtn>
      </MDBCardBody>
    </MDBCard>
  </div>
</template>

<script>
import {
  MDBCard,
  MDBCardBody,
  MDBCardTitle,
  MDBCardText,
  MDBCardImg,
  MDBBtn,
  mdbRipple,
} from "mdb-vue-ui-kit";
export default {
  components: {
    MDBCard,
    MDBCardBody,
    MDBCardTitle,
    MDBCardText,
    MDBCardImg,
    MDBBtn,
  },
  directives: {
    mdbRipple,
  },
  name: "Card",
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
  created() {
    document.body.style.backgroundColor = "black";
  },
};
</script>

<style></style>
