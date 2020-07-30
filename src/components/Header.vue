<template>
  <div class="header">
    <VueLogo class="logo" alt="logo" />
    <nav>
      <ul class="header__links">
        <li>
          <a href="#">Services</a>
        </li>
        <li>
          <a href="#">Projects</a>
        </li>
        <li>
          <a href="#">About</a>
        </li>
      </ul>
    <a href="#" class="cta"><button>Contact</button></a>
    </nav>
  </div>
</template>

<script>
import VueLogo from '@/img/logo.svg'

export default {
  components: {
    VueLogo
  }
}
</script>
