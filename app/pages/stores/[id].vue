<script setup lang="ts">
const route = useRoute()
</script>

<template>
  <h1>{{ route.params.name }}</h1>
  <p>{{ route.params.descriptions }}</p>
  <p>{{ route.params.vendor }}</p>
</template>

