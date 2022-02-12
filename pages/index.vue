<template>
  <Tutorial />
</template>

<script setup>
// import Vue from 'vue'
// import VueCompositionAPI from '@vue/composition-api'
// Vue.use(VueCompositionAPI)

// import {
//   getCurrentInstance
// } from '@vue/composition-api'

//  const instance = getCurrentInstance() 
//   const vm = instance?.proxy || instance
//   console.log(vm)


import useSWRV from "swrv";
const endpoint = "https://jsonplaceholder.typicode.com/users";
const { data, error } = useSWRV(endpoint, undefined);
console.log(`data ${JSON.stringify(data)} error ${JSON.stringify(error)}`);
</script>
