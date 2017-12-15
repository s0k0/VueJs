<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>
      Say hello to Vue.Js : <input id="inputGreeting" v-on:keyup="newGreeting">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App! Come in and find out :D'
    }
  },
  methods: {
    newGreeting: function () {
      var input = document.getElementById('inputGreeting')

      if (input.value !== '') {
        this.msg = input.value
      } else {
        this.msg = 'Welcome to Your Vue.js App'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
