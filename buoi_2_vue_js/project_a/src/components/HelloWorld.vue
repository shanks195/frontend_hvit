<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button v-on:click="deomSo">click</button>
    <h2>{{message}} and {{counter}}</h2>
    <h1 v-html="samHello"></h1>
    <p v-bind:id="islsdsd">Xin chao cac bạn</p>
    <button v-bind:disabled="disable">hello</button><br>
    <a v-bind:href="link">click vao day vao cong dong nay </a> <br>
    <button v-on:click="showAlert()">Hello Ai???</button>
  </div>
</template>

<script>

export default  {
 name:"HelloWorld",
 props: {
   msg:String
 },
 data() {
   return {
     link:"https://hvitclan.vn",
     disable:true,
     islsdsd:"Para",
    message: "Hello The Toan",
    counter: 0,
    samHello: '<p style="color:red">Hello teacher</p>'
   }

 },
 methods: {
   deomSo() {
     this.counter = this.counter + 1;
   },
   showAlert() {
     alert("hello teacher");
   }
 }
}
</script>
<style lang="scss">
   #Para {
   color:rgb(161, 127, 127);
   }
</style>

