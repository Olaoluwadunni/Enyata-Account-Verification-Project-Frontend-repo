<template>
    <div class="nav-bar">

        <div class="logo-img-wrapper">
        <router-link :to="{ name: 'Home'}"> 
            <img class="logo-img" src="../assets/verify-now-logo.svg" alt="logo" width="140" />
        </router-link>
        </div>
        <div id="nav">
             <ul>
                <!-- <li class="nav-links"><router-link :to="{name: 'Home'}">Home</router-link> </li> -->
            </ul>
        </div>
        <div class="btn">
            <router-link :to="{ name: 'Login'}">
                <Button buttonText="Login" btnStyle="login" />
            </router-link>
            <router-link :to="{ name: 'Sign Up'}">
                <Button buttonText="Sign Up For Free" :btnStyle="signUp" />
            </router-link>
        </div>
        <router-view />
  </div>
</template>

<script>
import Button from '@/components/Button.vue'

export default {
    name: 'NavBar',
    components: {
        Button
    },
    data () {
        return {
            signUp: 'sign-up-btn'
        }
    },
}
</script>

<style>
    .nav-bar {
        width: 100%;
        display: flex;
        justify-content: space-around;
    }
    .logo-img-wrapper {
        display: flex;
        flex-direction: row;
        padding-top: 30px;
        margin-top: auto;
        margin-bottom: auto;
    }
    ul {
        list-style-type: none;
        display: flex;
        flex-direction: row;
        padding-top: 30px;
        text-decoration: none;
    }
    li {
        margin-right: 50px;
        font-weight: 600;
        color: rgb(137, 145, 167);
        cursor: pointer;
    }
    a {
        text-decoration: none;
        color: rgb(137, 145, 167);
    }
    a:hover {
        color: #0066f5;
    }
    .router-link-exact-active {
        color: #0066f5;
    }
    .btn {
        display: flex;
        flex-direction: row;
        padding: 10px;
        margin-top: auto;
        margin-bottom: auto;
        padding-top: 30px;
    }
    .login {
        padding: 8px;
        background-color: #fff;
        border: 1px solid #0066f5;
        border-radius: 6px;
        outline: none;
        margin-right: 30px;
        width: 90px;
        font-family: 'Poppins';
        font-size: 14px;
        cursor: pointer;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 25px 50px -12px;
    }
    .login:hover {
        background-color: rgba(240, 240, 247, 0.61);
    }
    .sign-up-btn {
        padding: 10px;
        background-color: #0066f5;
        border: none;
        border-radius: 6px;
        outline: none;
        font-family: 'Poppins';
        font-size: 14px;
        cursor: pointer;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 25px 50px -12px;
        color: #fff;
    }
    .sign-up-btn:hover {
        background-color: #055eda;
    }
</style>