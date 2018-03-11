<template lang="pug">
  #app
    router-view/
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">

$green-light: #649257;
$green-dark: #487f39;
  
body, html {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  
}

body {
  font-size: 16px;
  line-height: 1.42;
}

.wrapper {
  overflow: hidden;
  min-height: 100%;
  position: relative;
}
#app {
  height: 100%;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

ul {
  list-style-type: none;
}


</style>
