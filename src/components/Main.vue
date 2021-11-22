<template>
  <main>
      <div class="main-left">
          <h1 class="main-head">Verify your bank<br/> account now</h1>
          <p class="main-text">{{ text }}</p>

        <div class="cta">
            <router-link :to="{ name: 'Sign Up'}">
                <Button buttonText="GET STARTED NOW" btnStyle="main-start-btn" />
            </router-link>
        </div>
      </div>
      <div class="main-img">

          <img src="../assets/bg-img.png" alt="img" />
      </div>
  </main>
</template>

<script>
import Button from '@/components/Button.vue'
export default {
    name: 'MainSection',
    components: {
        Button
    },
    data () {
        return {
            text: 'With our impressive and swift API option, you can easily verify your bank account in a twinkle of an eye'
        }
    }
}
</script>

<style>
    main {
        display: flex;
        flex-direction: row;
        width: 100%;
        margin-top: 80px;
    }
    .main-left {
        text-align: left;
        padding: 20px;
        margin-left: 140px;
        margin-top: 40px;
        color: rgb(20, 3, 94);
        width: 50%;
    }
    .main-head {
        font-size: 46px;
    }
    .main-text {
        font-weight: 100;
        width: 60%;
    }
     .cta {
        display: flex;
        flex-direction: row;
        margin-top: 40px;
    }
    .email-input {
        padding: 13px;
        outline: none;
        border: 1px solid #0066f55b;
        font-family: 'Poppins';
        font-size: 14px;
        border-radius: 8px;
        margin-right: 20px;
    }
    .main-start-btn {
        background-color: #0066f5;
        padding: 13px;
        border: none;
        outline: none;
        color: #fff;
        font-family: Poppins;
        font-size: 14px;
        border-radius: 8px;
        font-weight: 400;
        cursor: pointer;
    }
    .main-start-btn:hover {
        background: #055eda;
    }
    .main-img {
        width: 50%;
    }
</style>