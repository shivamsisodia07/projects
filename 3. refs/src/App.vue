<script setup>
import {ref} from "vue"
let obj3=ref({count:ref(0)});

setTimeout(()=>{

    console.log(obj3);
    console.log(obj3.value);
    console.log(obj3.value.count);
    console.log(obj3.count.value);

},2000)

</script>

<template>
    <div>hello</div>
</template>

<style scoped>

</style>
