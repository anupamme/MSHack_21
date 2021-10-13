<template>
  <div id="app">
    <div id="nav">
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
@import './assets/css/common.scss';
#app {
  font-family: 'Space Grotesk', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffffde;
}
body{
  background-color: #091b1f;
  margin: 0;
  font-family: 'Space Grotesk', sans-serif;
}
::-webkit-scrollbar {
  width: 5px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey;
  border-radius: 0px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #eb9472;
  border-radius: 0px;
}

</style>
