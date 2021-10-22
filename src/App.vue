<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>



  <router-view/>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
$color1: #333033B8;
$color2: #EE3191EF;
$color3: #f8e9f8;

.scrollbar{
  color: $color1;
}

#app {
  h1, h2{
    font-family: 'Cookie', cursive;
  }
  body{
    padding: 0;
    margin:0;
    background-color: $color1;
  }
  font-family: 'Overlock', cursive;;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: $color1;


}

#nav {
  padding: 30px;
  background-color: $color3;
  a {
    font-weight: bold;
    color: $color1;

    &.router-link-exact-active {
      color: #43408a;
    }
  }
}

</style>
