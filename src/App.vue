<template>
  <div id="app">
    <h1>WE ARE HERE.</h1>
    <input v-model="newDialog">
    <button @click="addDialog">Add dialogue</button>
    <ol>
      <li v-for="dialog in dialogs">{{dialog}}</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      newDialog: "Y-yo.",
      dialogs: ["I like frogs", "Look at the time!", "This party's over"]
    };
  },
  methods: {
    addDialog() {
      //alert("Hey Papi, can you make this thing work?")
      this.dialogs.push(this.newDialog);
      this.newDialog = "";
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
