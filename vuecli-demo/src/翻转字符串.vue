<template>
  <div >
    <h1>{{msg}}</h1>
    <button @click="toggle">翻转</button>
  </div>
</template>

<script>


export default {
 data(){
  return{
    msg:"hello world!"
  }
 },
 methods: {
  toggle(){
    let arr = this.msg.split('')
    console.log(arr);
    // console.log(arr.reverse());
    this.msg = arr.reverse().join('');
  }
 }
 
}
</script>

<style>

</style>
