<template>
<div class="tv">  
  <div class="container">
    <div class="inner">
      <div v-if="!isOn">
            <!-- <video src="require('src/public/vid1.mp4')" autoplay muted controls> </video> -->
            <img id="pic" src="../public/oil-gas.jpg" alt="">
        </div>
        <div v-else></div>
    </div> 
    <div class="buttons">
      <a @click="prev">
        <img src= '../public/previous.svg' />
      </a>
      <a @click="powerbtn">
        <img src="../public/powerbutton.svg" />
      </a>
      <a @click="next">
        <img src= '../public/next.svg' />
      </a>
    </div>
  </div>
</div>
 
</template>



<script>
export default {
  name: 'TelevisionPage',
  data(){
    return{
      isOn: true,
  }
},
methods:{
  powerbtn(){
    this.isOn = !this.isOn
  },
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
    .container {
  background-color:rgb(184, 241, 28);
  width: 700px;
  height: 500px;
  margin-top: 50px;
  padding: 10px;
  display: flex;
  flex-direction: column;
  border-radius: 5px;
}
.inner {
  background-color: rgb(7, 7, 7);
  width: 680px;
  height: 500px;
  border-radius: 5px;
}
img {
    height: 40px;
    margin: 5px;
}
.buttons {
  display: flex;
  justify-content: center;
}
#pic{
  width: 680px;
  height: 414px;
  border-radius: 5px;
}
</style>
