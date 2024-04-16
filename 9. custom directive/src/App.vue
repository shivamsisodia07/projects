<script setup>
// custom directives
// const vFontSize={
//   mounted:(el,binding) =>{
//     console.log(el);
//     console.log(binding);
//     el.style.fontSize=binding.value+"px";
//   },
// };

// const vFontSize={
//   mounted:(el,binding) =>{
//     console.log(el);
//     console.log(binding);
//     console.log(binding.modifiers);
//     // el.style.fontSize=binding.arg;with arg
//     if(binding.modifiers.large){
//       el.style.fontSize="10px";
//     }
//   },
// };


//shorthand
//this will be called for both mounted and updated
const vFontSize=(el,binding)=>{
  console.log(el);
    console.log(binding);
    console.log(binding.modifiers);
    // el.style.fontSize=binding.arg;with arg
    if(binding.modifiers.large){
      el.style.fontSize="10px";
    }
};

</script>

<template>
  <!-- <h2>hello</h2> -->
  <!-- <div v-font-size='60' >with passing value</div> -->
  
  <!-- <div v-font-size:small>with argument</div>
  <div v-font-size:large>with argument</div> -->

  <div v-font-size.modifiers.large >with modifiers</div>
</template>


