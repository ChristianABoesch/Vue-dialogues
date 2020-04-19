<template>
  <div id="app">
    <h1>WE ARE HERE.</h1>
    <select v-model="selected">
      <option disabled value>Please select one</option>
      <option>Joanna</option>
      <option>Matthew</option>
      <option>Watibushawa</option>
    </select>
    <input v-model="newDialog">
    <button @click="addDialog">Add dialogue</button>
    <button @click="dialogs=[]">Reset</button>
    <button @click="fixit('Hey Papi, this needs to be implemented.')">Play All</button>

    <ul>
      <li v-for="dialog in dialogs">
        <button @click="fixit('Hey Papi, this needs to be implemented.')">Play</button>
        <span>{{dialog}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      selected: "Joanna",
      newDialog: "Y-yo.",
      dialogs: ["I like frogs", "Look at the time!", "This party's over"]
    };
  },
  methods: {
    addDialog() {
      //alert("Hey Papi, can you make this thing work?")
      this.dialogs.push(this.newDialog);
      this.newDialog = "";
    },
    fixit(message) {
      alert(message);
    }
  }
};
</script>
