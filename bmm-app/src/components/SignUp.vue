<template>
  <div class="main">
    <h1>Welcome to Signup Page </h1>
    <input v-model="username">
    <p> {{ username  }}</p>
    <Workout :msg="username" :workouts="workouts" />
    <button v-on:click="getUsername"> Submit </button>
  </div>
</template>

<script>
 import Workout from './Workout.vue'
export default {
  name: 'SignUp',
 data: function() {
     return {
         username: 'londo farmer',
         workouts: [
           1,2
         ]
     }
 },
 components: {
     Workout,
  },
 methods: {
    getUsername: function() {
        console.log(this.username)
        if(this.username !== 'Londo') {
            this.username = "invalid"
        }


    }
 },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
