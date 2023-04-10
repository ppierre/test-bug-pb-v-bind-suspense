<script setup lang="ts">
//import PocketBase, { Record } from 'pocketbase'
import Card from '@/components/Card.vue'

class Record {
  id: number
  value: string

  constructor(obj: { id: number; value: string }) {
    this.id = obj.id
    this.value = obj.value
  }

  $load(value: string) {
    this.value = value
    console.log(value)
  }
}

const events: Record[] = [
  new Record({ id: 1, value: '11' }),
  new Record({ id: 2, value: '22' }),
  new Record({ id: 3, value: '33' })
]
debugger
</script>

<template>
  <main>
    <card v-for="event in events" v-bind="event" :key="event.id" />
  </main>
</template>
