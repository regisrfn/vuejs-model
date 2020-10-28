<template>
  <div class="header" :class="{ scrollClass: isActive }">
    <VueLogo class="logo" alt="logo" />
    <nav>
      <ul class="header__links hidden-menu">
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">Information</a>
        </li>
        <li>
          <a href="#">About</a>
        </li>
        <button>Services</button>
      </ul>      
    </nav>
    <nav>
      <ul class="header__links header__register">
        <li>
          <a href="#">Login</a>
        </li>
        <li>
          <a href="#">Register</a>
        </li>
      </ul>
    </nav>

    <input type="checkbox" class="header__btn" id="navbar-btn" />
    <label for="navbar-btn" class="navbar-icon">
      <span class="navbar-icon__line"></span>
    </label>
  </div>
</template>

<script>
import VueLogo from "@/img/logo.svg";

export default {
  data() {
    return {
      isActive: false,
    };
  },
  components: {
    VueLogo,
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll(event) {
      const scrollY = window.scrollY;
      if (scrollY > 10) {
        this.isActive = true;
      } else {
        this.isActive = false;
      }
    },
  },
};
</script>