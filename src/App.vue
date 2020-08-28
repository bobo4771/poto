<template>
 <div id="app">
 
    <HelloWorld bobo="ประเทศไทย" />
    <hr>
    <div class="row">
      <div class="col-6">
   <img src="./assets/prao1.png" width="500" height="300" /> 
     
     
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
  <img src="./assets/paro.png" width="350" height="300" />
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CsButton @cc="sum" />
      </div>
      <div class="col-6">
        <CsButton @cc="sem" />
      </div>
    </div>
    
  </div>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsButton from "./components/CsButton.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
    
  },
  data : function(){
    return {
    total1: 0,
    total2: 0,
   
   } 
  },
  methods: {
  sum(counterValue){
    this.total1 = counterValue
  },
  
  sem(counterValue){
    this.total2 = counterValue
 
  
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
  color: #0b44ff;
  margin-top: 60px;
  
}
body {
background-image: url("./assets/bg.jpg");
  background-size: 100%;
}
</style>

