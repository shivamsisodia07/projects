<script setup>
import {ref,onUnmounted,onMounted} from 'vue';
import {faker} from '@faker-js/faker';

const firstName=ref("");
const lastName=ref("");

function updateDetails(){
  firstName.value=faker.person.firstName.name;
  lastName.value=faker.person.lastName.name;
  console.log(faker.person);
}

onMounted(()=>{window.addEventListener("mousemove",updateDetails);});
onUnmounted(()=>{window.addEventListener("mousemove",updateDetails);});

</script>

<template>
  <h2>hello</h2>

  <h2>firstName:{{ firstName }}</h2>
  <h2>lastName:{{ lastName }}</h2>
</template>

