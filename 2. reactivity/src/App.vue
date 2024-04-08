<!-- reactivity -->
<!-- <script setup>
import {reactive} from 'vue';
    
let num=reactive({count:0});
    setTimeout(()=>
      {
        console.log(num.count);
        num.count++;
        console.log(num.count);
      }
    ,2000);
</script>

<template>
 <h1>{{num.count}}</h1>
</template> -->


<!-- deep reactivity -->

<script setup>
import {reactive} from 'vue';
    
let obj=reactive({
  
  num:{count:0},
  names:["rahul","shivam"],
  });
    setTimeout(()=>
      {
        console.log(obj.num.count);
        obj.num.count++;
        obj.names.push("ram");
        console.log(obj.num.count);
        console.log(obj.names);
      }
    ,2000);
</script>

<template>
 <h1>{{obj.num.count}}</h1>
 <h1>{{ obj.names}}</h1>
  <!-- console.log(obj.num.count); -->
</template> 

