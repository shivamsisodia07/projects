<script setup>
   import {inject,ref} from 'vue'
    
    const name=inject("name","rahul");
    const count=inject("cnt","0");
    // const count=ref(0);
    function handleclick(){
        count.value++;
        console.log(count.value);
    };
</script>


<template>
    <h1>
        guest
    </h1>
    <h2>value:{{ count }}</h2>
    <button @click="handleclick" >click me</button>
    
</template>

<script scope>
export default{
    name:'Guest'
}
</script>