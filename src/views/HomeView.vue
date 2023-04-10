<script setup lang="ts">
import PocketBase, { Record } from 'pocketbase'
import Card from '@/components/Card.vue'

const events: Record[] = await new Promise((resolve) => {
  setTimeout(
    () =>
      resolve([
        new Record({ id: 1, value: '11' }),
        new Record({ id: 2, value: '22' }),
        new Record({ id: 3, value: '33' })
      ]),
    500
  )
})
</script>

<template>
  <main>
    <card v-for="event in events" v-bind="event" :key="event.id" />
  </main>
</template>
