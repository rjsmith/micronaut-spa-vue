<template>
  <div>

    <form v-on:submit.prevent="getMessage">
      <label>Enter your name: </label>
      <input type="text" v-model="name" />
      <input type="submit" value="Submit" />
    </form>

    <p>
      {{ message }}
    </p>

  </div>
</template>

<script>

import {SERVER_URL} from "../config";

export default {
  name: "Micronaut",

  data: function () {
    return {
      name: "World",
      message: null
    }
  },

  methods: {
    getMessage: function () {
      fetch(`${SERVER_URL}/${this.name}`)
        .then(r => r.text())
        .then(message => this.message = message)
        .catch(e => console.error(e))
    }
  }
}
</script>