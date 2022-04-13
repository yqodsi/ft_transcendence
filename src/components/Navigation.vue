<template>
  <header>
    <nav class="container">
      <div class="branding">
        <router-link class="header" to="home">PONG ⚫</router-link>
        <!-- <div>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        </div> -->
      </div>
      <div class="nav-links">
        <ul v-show="!mobile">
          <router-link class="link" to="home">home</router-link>
          <router-link class="link" to="#">Blogs</router-link>
          <router-link class="link" to="about">Create Post</router-link>
          <a class="login-btn" href="#!" role="button">
            <!-- <MDBBtn
              color="warning"
              style="background-color: #f10086; font-weight: 600"
              rounded
              >Login</MDBBtn -->
            <!-- > -->
            <a>
              <img class="img-42" src="../assets/img.png" />
            </a>
          </a>
        </ul>
      </div>
    </nav>
    <transition
      name="menu-icon"
      appear
      appear-class="custom-appear-class"
      appear-active-class="animated bounceIn"
    >
      <a
        class="m-1 menu-icon"
        href="#!"
        role="button"
        style="color: #f10086"
        @click="toggleMobileNav"
        v-show="mobile"
      >
        <MDBIcon icon="bars" size="lg"></MDBIcon>
      </a>
    </transition>
    <transition
      name="mobile-nav"
      appear
      appear-class="custom-appear-class"
      appear-active-class="animated bounceIn"
    >
      <ul class="mobile-nav" v-show="mobileNav">
        <a
          class="m-1 menu-icon"
          href="#!"
          role="button"
          style="color: #f10086"
          @click="toggleMobileNav"
          v-show="mobile"
        >
          <MDBIcon icon="times" size="lg"></MDBIcon>
        </a>
        <router-link class="link" to="home">Home</router-link>
        <router-link class="link" to="about">Blogs</router-link>
        <router-link class="link" to="home">Create Post</router-link>
        <MDBBtn size="lg" color="primary" floating>
          <MDBIcon icon="sign-in-alt"></MDBIcon>
        </MDBBtn>
        <a class="login-side-btn" href="#!" role="button">
          <MDBBtn style="background-color: #f10086; color: white" rounded
            >Login</MDBBtn
          >
        </a>
      </ul>
    </transition>
  </header>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import { MDBIcon, MDBBtn } from "mdb-vue-ui-kit";
export default defineComponent({
  name: "App",
  components: {
    MDBIcon,
    MDBBtn,
  },
  data() {
    return {
      mobile: false as boolean,
      mobileNav: false as boolean,
      windowWidth: null as number | null,
      windowtop: null as number | null,
    };
  },
  created() {
    window.addEventListener("resize", this.checkScreenSize); // check screen size on resize
    this.checkScreenSize(); // check on page load
  },
  methods: {
    checkScreenSize() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 780) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },

    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },
  },
});
</script>

<style lang="scss" scoped>
header {
  background-color: transparent;
  padding: 0 25px;
  // box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
  //   0 2px 4px -1px rgba(0, 0, 0, 0.06);
  z-index: 99;
}
.link {
  font-weight: 400;
  padding: 0 8px;
  transition: 0.3s color ease;
  &:hover {
    color: #1eb8b8;
  }
}
nav {
  // gap: 20rem;
  display: flex;
  padding: 25px 0;
  // border: 1px solid red;
  height: 4rem;

  .branding {
    // display: flex;
    // justify-self: flex-start;
    // align-items: center;
    top: 14px;
    left: 25px;
    position: fixed;
    .header {
      color: white;
      font-size: 24px;
      font-weight: 700;
      text-decoration: none;
    }
  }

  .nav-links {
    display: flex;
    position: sticky;
    top: 0;
    flex: 1;
    align-items: center;
    justify-content: center;
    ul {
      margin: 0;
      margin-right: 32px;
      .link {
        margin-right: 32px;
        font-weight: 400;
        font-size: 16px;
        color: white;
      }
      .link:last-child {
        margin-right: 0;
      }
    }
  }
}

.menu-icon {
  position: fixed;
  top: 14px;
  right: 25px;
  cursor: pointer;
  width: 25px;
  height: 25px;
}
.mobile-nav {
  padding: 25px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: fixed;
  height: 100%;
  background-color: #93b5c6;
  top: 0;
  left: 0;
  .link {
    color: #041c32;
    font-weight: 600;
    padding: 15px;
  }
}
.login-btn {
  position: fixed;
  right: 50px;
  top: 12px;
  cursor: pointer;
  font-weight: 700;
}
.login-side-btn {
  padding: 10px;
  cursor: pointer;
}
.img-42 {
  width: 45px;
  top: 15px;
  right: 15px;
  position: fixed;
  aspect-ratio: 1;
  border-radius: 20px;
}
.mobile-nav-enter-active,
.mobile-nav-leave-active {
  transition: all 0.8s ease;
}
.mobile-nav-enter-to {
  transform: translateX(0);
}
.mobile-nav-enter-from {
  transform: translateX(600px);
}
.mobile-nav-enter-from {
  transform: translateX(-1000px);
}
.mobile-nav-leave-to {
  transform: translateX(-1000px);
}
</style>
