<template>
  <div class="container">
    <div class="imglist">
      <h3>图片列表区</h3> 
      <img src="./assets/01.jpg" alt=""  @mouseover="imgFn(1)" @click="imgSrc($event)">
      <img src="./assets/02.jpg" alt=""  @mouseover="imgFn(2)" @click="imgSrc($event)">
      <img src="./assets/03.jpg" alt=""  @mouseover="imgFn(3)" @click="imgSrc($event)">
    </div>
    <div class="show">
      <h3>图片预览区</h3>
      <img v-bind:src="imgUrl" alt="" style="width:600px;height:auto;">
    </div>
   <div>
   </div>
  </div>
</template>

<script>
import img1 from './assets/01.jpg'
import img2 from './assets/02.jpg'
import img3 from './assets/03.jpg'
export default {
  data(){
    return{
      imgUrl:img1
    }
  },
  methods: {
    imgFn(val){
     this.imgUrl={1:img1,2:img2,3:img3}[val]
    },
    imgSrc(e){
      
     alert(e.target.src)
    }
  }
};
</script>

<style scoped>
  .container {
    display:flex;
  }
 .imglist { 
  border: 2px solid red;
 }
.imglist img {
  width: 200px;
  height: auto;
}
.show {
  border: 2px solid red;
  margin-right: 20px;
}

</style>