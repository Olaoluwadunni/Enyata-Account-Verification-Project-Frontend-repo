<template>
  <main>
      <div class="main-left">
          <h1 class="main-head">Log in to your account</h1>

          <form>
            <input class="email-input" v-model="email" type="email" placeholder="Your email..." />
            <input class="email-input" v-model="password" type="password" placeholder="Your password..." />

            <div class="cta">
                <button @click.prevent="login" class="main-start-btn">LOG IN</button>
            </div>
          </form>
      </div>
      <div class="main-img">
          <img src="../assets/bg-img.png" alt="img" />
      </div>
  </main>
</template>

<script>
// import Button from '@/components/Button.vue'
// import Button from './Button.vue'
import axios from 'axios'
export default {
    name: 'LoginMain',
    components: {
        // Button
        // Button
    },
    data () {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        async login() {
            let res = await axios.post('http://localhost:2000/api/login-user', {
                email: this.email,
                password: this.password
            });
            console.warn(res)
            if (res.status === 200) {
                this.clearInfo()
                console.log('Login successfully')
                // this.$router.push({name:'Successfully Created'})
            } else {
                console.log('error')
            }
        },
        clearInfo() {
            this.email = '',
            this.password = ''
        },
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
        width: 60%;
        margin-right: 20px;
        margin-top: 30px;
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
        width: 440px;
    }
    .main-start-btn:hover {
        background: #055eda;
    }
    .main-img {
        width: 50%;
    }
</style>