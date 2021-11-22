<template>
    <div>
        <LandingPageNavBar />
        <LoginMain />
    </div>
</template>

<script>
import LandingPageNavBar from "@/components/LandingPageNavBar.vue"
import LoginMain from "@/components/LoginMain.vue"
export default {
    name: 'SignUp',
    components: {
        LandingPageNavBar,
        LoginMain
    }

}
</script>

<style>

</style>