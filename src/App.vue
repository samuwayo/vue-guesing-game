<template>
  <router-view class="router"/>
</template>

<style>
*{

   font-family: "Briem Hand";
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body{
  background-image: url('./assets/background.jpg');
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
  background-position: center;
  background-size: cover;
  overflow: hidden;
  margin: 0;
  padding: 0;
  font-family: "Briem Hand";
}
.logo{
  position: absolute;
  width: 50px;
  left: 0;
  margin-left: 60px;
}
nav {
  padding: 10px 25px;
  background-color: transparent;
  width: 100vw;
  margin-bottom: 20px;
  /* box-shadow: 0 0 50px #000; */
}

nav a {
  font-weight: bold;
  color: #fff;
  margin: 0 20px;
  text-decoration: none;
  font-size: 25px;
  font-weight: bold;
}

nav a.router-link-exact-active {
  color: #e1510e;
  background-color: transparent;
  text-decoration: none;
}

.router{
  
  width: 100vw;
  height: 100vh;
  margin-top: 0;

}
</style>
