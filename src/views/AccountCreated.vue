<template>
    <div>
        <LandingPageNavBar />
        <AccountSuccessMain />
    </div>
</template>

<script>
import LandingPageNavBar from "@/components/LandingPageNavBar.vue";
import AccountSuccessMain from "@/components/AccountSuccessMain.vue";
export default {
    name: 'AccountCreated',
    components: {
        LandingPageNavBar,
        AccountSuccessMain
    }

}
</script>