<template>
  <div id="app">
    <div class="title">
      <!-- <img src="./assets/elephant-doodle.jpg" alt="" class="elephant" /> -->
      <img alt="ERGO logo" src="./assets/ergo-logo-gray.png" class="logo" />
      <h1>
        's White Elephant
      </h1>
    </div>

    <List />
  </div>
</template>

<script>
import List from "./components/List.vue"

export default {
  name: "App",
  components: {
    List,
  },
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;1,300&display=swap");
#app {
  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #53565a;
  width: 100%;
  height: 100%;
  margin: 0;
  background-image: url("./assets/Snowflake-Pattern.jpg");
  background-size: 100px;
  background-repeat: repeat;
}

.title {
  display: flex;
  justify-content: center;
  align-items: center;
}

.elephant {
  width: 150px;
  margin-right: 20px;
}

.logo {
  width: 180px;
}

h1 {
  font-size: 3.2em;
}
</style>
