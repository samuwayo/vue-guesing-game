<template>
   <nav>
      
      <img src="../assets/logo (2).png" class="logo" alt="">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/sam">Sam</router-link>
  </nav>
  <div class="home">
    <div class="levels" >
      <div v-for="level in levels" :key="level.level">
      <div class="div">
        <br>
        <span>{{ level.level }}</span>
        <br>
       <span> {{ level.number }}</span>
      </div>
      </div>
    </div>
  </div>
  <router-link to="/about"><button>start</button></router-link>
  
</template>

<script setup>
 const levels = [
  {
    level: "level 1",
    number: "1-9"
  },
  {
    level: "level 2",
    number: "1-19"
  },
  {
    level: "level 3",
    number: "1-39"
  },
  {
    level: "level 4",
    number: "1-39"
  }
 ]
  // return {levels}
</script>
<style>
.levels{
  justify-content: center;
  display: flex;
  flex-wrap: wrap;
  font-family: "Briem Hand";
  margin-top: 60px;
}
.div{
  border-radius: 50px 50px 50px 50px / 25px 25px 25px 25px;
  display: flex;
  border: 20px solid;
  /* border image */
  border-image-source: url('../assets/background2.jpg');
  box-shadow: 2px 2px 30px rgba(0, 0, 0,0.99) inset;
  border:  10px solid #ef660b;
/* border image */
  width: 230px;
  height: 230px;
  text-align: center;
  margin: 30px;
  font-size: 50px;
  color: #ef660b;
  justify-content: center;
  display: block;
  transform: skew(15deg, 15deg);;
}
span{
margin-top: 30px;
}
button{
  background-image: url('../assets/background.jpg');
  width: 200px;
  height: 70px;
  font-size: 40px;
  color: #ef660b;
  text-align: center;
  border-radius: 10px 20px;
  border: 2px solid #ef660b;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  margin-top: 50px;

}
</style>