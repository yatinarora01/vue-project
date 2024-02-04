<template>
  <div>
  <img class="logo" src="../assets/istockphoto-981368726-612x612.jpg" alt="restaurant logo">
  <h1>sign up</h1>
  <div class="register">
      <input type="text" v-model="name" placeholder="enter your name">
      <input type="email" v-model="email" placeholder="enter your email">
      <input type="password" v-model="password" placeholder="enter your password">
      <button v-on:click="signup">Sign Up</button>
  
      <router-link :to="{ name: 'home' }" class="nav-link">Go to Home</router-link>
    </div>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  name: 'signup',
  data()
  {
      return{
          name:'',
          email: '',
          password: ''

      }
  },
  methods:{
     async signup()
      {

          let result = await axios.post("http://localhost:3000/user",{
              email : this.email,
              password : this.password,
              name : this.name
          });

          console.log(result);
          if(result.status ==201)
          {

              localStorage.setItem("user-info",JSON.stringify(result.data))
              this.$router.push({name:'home'})
          }

          }
  }

}

</script>

<style>
.logo{
  width: 200px;

}
.register input {
  width: 300px;
  height: 40px;
  padding-left: 20px;
  display: block;
  margin-bottom: 30px;
  margin-right:auto ;
  margin-left: auto;
  border: 1px solid skyblue;
}

.register button{
  width: 320px;
  height: 40px;
  border: 1px solid aqua;
  background-color: white;
  color: aqua;
  cursor: pointer;
  font-size: large ;
  font-weight: bold;


}



</style>

