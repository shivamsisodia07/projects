<script setup>
const msg="hello";
const attribute="id";
const isdisabled=false;
function disp(){
  console.log("hi function")
}
</script>
<template>
  <div>hello</div>
  <br>
  <div>{{2*10}}</div>
  <br>
  <div>{{ msg }}</div>
  <br>
  <div>{{ disp() }}</div>
  <br>

  <div :[attribute]="msg" >hi</div>


  <button :disabled="isdisabled" >click me</button>
</template>

<style scoped>

</style>
