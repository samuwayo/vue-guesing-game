<template>
  <div class="about">
   <nav class="gamenav">
    <div class="logo">
      <img src="../assets/logo (2).png" class="logo" alt="">
    </div>
    <div class="menus">
      <div class="level">level: 1</div>
      <div class="score">wins:{{ win }}</div>
      <div class="score">wins:3 >></div>
      <div class="score">screat is: {{ screat }}</div>
    </div>
   </nav>
   <div class="out">{{ wins }}</div>


   <div class="counter">
    
    <span class="num">{{ count }}</span>
    
   </div><br>

   
 <div class="btns">
   <div v-for="btn in buttons" :key="btn.text" :class="btn.class">
    
    <router-link to="/about"><button v-on:click="guessing( btn.text )">{{ btn.text }}</button></router-link>
    
  
  </div>

  
 </div>





  </div>
  
</template>   
   <script setup>

import { ref } from 'vue';
 
   let win=ref(0);
  let loss = ref(0);
  
let screat= ref(null);
    
     
     let wins = ref('level 1'); 
     let count = ref(0);
    // let numb;
     function counter(){
      setInterval(()=>{
        
        if(count.value < 9){
          count.value += 1;
        }
        else{

          count.value = 0;

        }

      // numb = count;
      }
      
      ,50)
     }

     counter();
       const buttons = [
       {
          text:0,
          class:"btn",
        },
        {
          text:1,
          class:"btn"
        },
        {
          text:2,
          class:"btn"
        },
        {
          text:3,
          class:"btn"
        },
        {
          text:4,
          class:"btn"
        },
        {
          text:5,
          class:"btn"
        },
        {
          text:6,
          class:"btn"
        },
        {
          text:7,
          class:"btn"
        },
        {
          text:8,
          class:"btn"
        },
        {
          text:9,
          class:"btn"
        }
       ];
      function Timeout(){
       setTimeout(() => {
        wins.value = '';
       }, 1500);
      }
       const guessing = (btn)=>{
        const random = Math.floor((Math.random())*10);
     
        screat.value = random;
        Timeout();
        if(btn.toString() == random.toString()){
          wins.value = 'YOU WIN';
          win.value ++;
        }
        else{
          wins.value = 'YOU LOOSE';
          loss.value ++;
        }
    
      }    
  



   </script>
   
   
   <style scoped>

 /* taggel next btn */
#none{
  
    display: none;
}
#flex{
  display: flex;
}



  .next{
       bottom: 60px;
       position: absolute;
       font-size: 20px;
       border: none;
       background: transparent;
  }
  .next h1{
    text-decoration: none;
    color: #ef660b;
    padding-bottom: 40px;
  }
    .gamenav{
     width: 100vw;
     display: flex;
     justify-content: center;
     color: #ef660b;
    }
    .menus{
     display: flex;
    }
    .menus div{
     display: flex;
     padding-top: 10px;
     margin-inline: 80px;
     font-size: 30px;
    }
    .counter{
     width: 300px;
     height: 300px;
     /* border: #ef660b 3px solid; */
     font-size: 100px;
     color: #fff;
     margin-top: 150px;
     border-radius: 50%;
     border: #ef660b solid 10px;
     font-size: 100px;
     justify-content: center;
     /* display: flex; */
     display: flex;
     position: absolute;
     right: 40%;
     
     z-index: -1;
       content: '';
       width: 250px;
       height: 250px;
       /* border: 1px solid #ef660b; */
      animation: color infinite 1s;
       
   
    }
   .btns{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
   }
   button{
    margin: 20px;
    width: 100px;
    height: 35px;
    font-size: 20px;
   }
   
   
   .out{
    color: #fff;
    font-size: 50px;
   }
   .btns .btn{
    color: #ef660b;
   }
   .num{

    margin-top: 50px;
   }
   
   /* for animations */


   @keyframes color {
     from {
             
             font-size: 100px;
    
    }
     to {
             
             font-size: 70px;
    }
    }
    

   
   
   
   
   
   
   
   
   
   
   
   
   </style>