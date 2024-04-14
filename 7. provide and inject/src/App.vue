<script setup>
import User from './components/user.vue';
import {provide} from 'vue';
import {ref} from 'vue';

provide("name","shivam");//providing string
const cnt=ref(0);//providing ref

provide("cnt",cnt);
</script>

<template>
  <h2></h2>
  <h2>ref value on clicking button in guest component:{{cnt}}</h2>
  <User></User>
</template>
