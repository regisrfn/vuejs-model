<template>
  <div class="header">
    <VueLogo class="logo" alt="logo" />
    <nav>
      <ul class="header__links">
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">Information</a>
        </li>
        <li>
          <a href="#">About</a>
        </li>
      </ul>
    <button>Services</button>
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
