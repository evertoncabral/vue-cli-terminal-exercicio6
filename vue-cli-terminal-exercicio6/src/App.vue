<template>
  <div id="app">
    <input type="text" v-model="text" />
    <br />
    <span>Text: {{ text }}</span> 
    <br />
    <span>API: {{ apiResponse }}</span>
  </div>
</template>



<script>
export default {
  name: "App",
  data() {
    return {
      apiResponse: "Start",
      text: 123,
    };
  },
  methods: {
    // simulateAPI(response) {
    //   return new Promise((res) => {
    //     setTimeout(() => {
    //       this.apiResponse = response;
    //     }, 1000);
    //   });
    // },
    async fetchAPI(value) {
      await this.simulateAPI(value);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
