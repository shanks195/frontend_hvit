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
    <button v-on:click="demcuu">Dem cuu</button>
<p>{{counter}} con cuu</p>
<button v-on:click="demcuux2">Dem cuu</button>
<button v-on:click="demcuu1(5)">Dem cuu</button>
<p>{{counter}} x2 con cuu</p>
<select v-on:change="chonkhoahoc" v-model="khoahoc">
	<option value="Fullstack java">Fullstack java</option>
	<option value="Fullstack php">Fullstack php</option>
	<option value="Fullstack javascript">Fullstack javascript</option>
	<option value="Fullstack C#">Fullstack C#</option>
<select>
<button v-on:click="counter1++">Tang cuu</button>
<br>
<br>
<button v-on:click="counter1++">Giam  cuu</button>
bộ dếm: {{counter1}}
{{ res }} | {{ deomcuu()}} số cưu

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
    counter1:0,
    samHello: '<p style="color:red">Hello teacher</p>',
    khoahoc:'',
   }

 },
 computed:{
   res() {
     this.counter1 >5? 'co nhieu hon 5' : 'co it hon 5';
   }
 },
 methods: {
    deomcuu() {
     this.counter1 >5? 'co nhieu hon 5' : 'co it hon 5';

   },
   deomSo() {
     this.counter = this.counter + 1;
   },
   showAlert() {
     alert("hello teacher");
   },
   demcuu() {
		this.counter++
		},
		demcuu1(SoNhan){
			this.counter=this.counter*SoNhan;
		},
		demcuux2() {
		this.counter=counter+2
		},
		chonkhoahoc() {
			var msg ='Ban vua chon khoa hoc' +this.khoahoc;
			alert(msg);
		}
 }
}
</script>
<style lang="scss">
   #Para {
   color:rgb(161, 127, 127);
   }
</style>

