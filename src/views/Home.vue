<template>
  <div class="home">
    <LandingPageNavBar />
    <Main />
  </div>
</template>

<script>

import LandingPageNavBar from "@/components/LandingPageNavBar.vue"
import Main from "@/components/Main.vue"
export default {
  name: "Home",
  components: {
    LandingPageNavBar,
    Main
  },
};
</script>
