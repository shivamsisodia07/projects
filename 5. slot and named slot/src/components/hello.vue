<script setup>

import customButton from './components/customButton.vue ';
const props=defineProps([
    "name",
    "count"
])
</script>


<template >
    // named slot
    // <slot name="header"></slot> 
    // <div>{{props.name}}</div>
    // <h2>{{ props.count+2 }}</h2>/
    // scoped slot
    // <slot nm="shivam" age="18" > </slot>

    <customButton></customButton>
</template>