<template>
    <div>
        <LandingPageNavBar />
        <SignUpMain />
        
    </div>
</template>

<script>
import LandingPageNavBar from "@/components/LandingPageNavBar.vue"
import SignUpMain from "@/components/SignUpMain.vue"
export default {
    name: 'SignUp',
    components: {
        LandingPageNavBar,
        SignUpMain
    }

}
</script>

<style>

</style>