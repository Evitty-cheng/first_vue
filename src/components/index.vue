<template>
  <div>
    <div>
      <p>{{message}}</p>
      <input v-model="message">
      <button v-on:click="reverseMessage">Reverse Message</button>
    </div>
    <ab-todo></ab-todo>
  </div>
</template>

<script>
import AbTodo from './ab-todo.vue'
export default {
  components: {
    AbTodo: AbTodo
  },
  data () {
    return {
      message: 'Hello Vue.js!'
    }
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
}
</script>

<style>
</style>
