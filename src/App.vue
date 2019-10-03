<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
body {
  width: 100%;
  height: 100%;
  background-color: $background;

  font-family: serenity, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: white;
  font-style: normal;

  &:before {
    content: "";
    position: fixed;
    width: 200vw;
    height: 200vh;
    top: -50%;
    left: -50%;
    z-index: -1;
    background: url('assets/bg.png') 0 0 repeat;
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg);
    opacity: 0.5;
  }
}
</style>
