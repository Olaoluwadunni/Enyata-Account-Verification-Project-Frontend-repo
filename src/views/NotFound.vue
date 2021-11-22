<template>
  <div>
    <LandingPagNavBar /> 
    <img class="error-img" src="../assets/error.svg" alt="error" />
      <!-- <h2>404</h2> -->
      <h3>Page Not Found</h3>
  </div>
</template>

<script>
import LandingPagNavBar from "@/components/LandingPageNavBar.vue";

export default {
    name: 'NotFound',
    components: {
        LandingPagNavBar
    }
}
</script>

<style>
.error-img {
    width: 400px;
    height: 400px;
}
</style>