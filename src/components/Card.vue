<script setup lang="ts">
defineProps({ id: String, value: String })
</script>

<template>
  <div>
    <h3>Card</h3>
    <p>id: {{ id }}</p>
    <p>value: {{ value }}</p>
  </div>
</template>
