  <script setup lang="ts">
 import { useUserStore } from '~~/stores/user'
   const userStore = useUserStore()
  </script>
<template>
    <div>
      <div>{{ userStore.user }}</div>
      <div> <button @click="userStore.save({ email: 'peterkimzz69@gmail.com' })">Increment</button></div>
    </div>
  </template>
  