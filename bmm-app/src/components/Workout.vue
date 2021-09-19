<template>
  <div class="hello">
    <h4 id="h4-style">Username: {{ msg }}</h4>
    <ul>
    <li> {{workouts}} </li>
    </ul>
      </div>
</template>

<script>
export default {
  name: 'Workout',
  props: {
    msg: String,
    workouts: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#h4-style {
  font-size: 40px
}
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
