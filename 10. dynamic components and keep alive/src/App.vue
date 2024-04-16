<!-- dynamic component -->

<!-- <script setup>
import user from './user.vue';
import guest from './guest.vue';
import popular from './popular.vue';
import {ref} from 'vue';
const currentTab=ref("user");
const tabs={
  user,guest,popular
}
</script>

<template>
  <h2>app</h2>


  <button v-for="(_,tab) in tabs" :key="tab" @click="currentTab=tab" >
    {{ tab }}</button>

  <component :is="tabs[currentTab]" ></component>

</template> -->


<!-- keep alive :to cache component-->

<script setup>
import user from './user.vue';
import guest from './guest.vue';
import popular from './popular.vue';
import { ref } from 'vue';
const currentTab = ref("user");
const tabs = {
  user, guest, popular
}
</script>

<template>
  <h2>app</h2>


  <button v-for="(_, tab) in tabs" :key="tab" @click="currentTab = tab">
    {{ tab }}</button>

  <!-- <KeepAlive>
  <component :is="tabs[currentTab]"></component>
  </KeepAlive>
-->
  <KeepAlive include="user,guest">
    <component :is="tabs[currentTab]"></component>
  </KeepAlive>

</template>