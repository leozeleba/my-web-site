<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  overflow: hidden;
  font: "Roboto";
}
* { margin: 0 ; }
ul{
  padding:0
}
li{
  list-style-type: none;
}

.row{
  display: flex;
}

video{
    max-width: 700px;
    align-self: auto;
}

</style>

