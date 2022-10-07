<template>
    <div>
      <h1 class="text-3xl font-bold">User</h1>
      <div v-if="pending">Loading..</div>
      <template v-else>
        <div v-if="error">Sorry, error occured.</div>
        <div v-else>{{ data }}</div>
      </template>

      <button @click="refresh()">Refresh</button>

    </div>
  </template>
  
  <script setup lang="ts">
  // const { data, pending, error, refresh } = await useFetch('https://jsonplaceholder.typicode.com/todos/1')
  const { data, pending, error, refresh } = await useApi('/todos/1')
  </script>