<template>
  <div >
    <span>选择所在地区：</span>
    <input type="radio" name="radio" value="中国大陆" v-model="area">中国大陆
    <input type="radio" name="radio" value="中国香港" v-model="area">中国香港
    <br>
    <span>手机号码：</span>
    <input type="text" v-model.number="phone">
    <br>
    <span>年龄：</span>
    <input type="text" v-model.number="age">
    <br>
    <span>密码：</span>
    <input type="password" v-model="pass">
    <br>
    <span>爱好：</span>
    <input type="checkbox" value="看书" v-model="hobby">看书
    <input type="checkbox" value="学习" v-model="hobby">学习
    <input type="checkbox" value="写代码" v-model="hobby">写代码
    <input type="checkbox" value="游戏" v-model="hobby">游戏
    <br>
    <input type="checkbox"  v-model="isAgree">记住密码
    <br><span>==========================</span>
    <div>
      我来自：{{area}}
      <br>
      手机号码是：{{phone}}
      <br>
      年龄是：{{age}}
      <br>
      密码是：{{pass}}
      <br>
      爱好是：{{hobby.join('-')}}
      <br>
      是否记住密码：{{isAgree?'是':"否"}}
    </div>
  </div>
  
</template>

<script>


export default {
 data(){
  return{
   area:'中国大陆',
   phone:'',
   age:'',
   pass:'',
   hobby:[],
   isAgree:''
  }
 },
 methods: {
  
 }
 
}
</script>

<style>

</style>
