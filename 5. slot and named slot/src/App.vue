<script setup>
import Hello from './components/hello.vue';
</script>

<template >
  
  <!-- <Hello name="shivam" count="2">
    named slot
    <template v-slot:header>  
      <h2>header</h2>
    </template>

    <div> dajfd</div>
  </Hello> -->

  <hello v-slot="slotProps" class="btn-pink">

    <h2>{{slotProps.nm}}</h2>
    <h2>{{slotProps.age}}</h2>
   
  </hello>

</template>
