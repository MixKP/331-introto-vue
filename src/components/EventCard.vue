<script setup lang="ts">
// defineProps<{
//   msg: string
// }>()

// const event = ref ({
//   id:5928101,
//   category: 'animal welfare',
//   title: 'Cat Adoption Day',
//   description: 'Find your new feline friend at this event.',
//   date: 'January 28, 2002',
//   time: '12:00',
//   petsAllowed: true,
//   organizer: 'Kat Laydee'
// })

import type { Event } from '@/type';
defineProps <{
  event: Event
}>()

</script>

<template>
  <div class="event-class">
    <div class="event-card">
      <h2>{{ event.title }}</h2>
      <span>@{{ event.time }} on {{ event.date }}</span>
    </div>
  </div>
</template>
<style scoped>
.event-class {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}
.event-class:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px rgba(0, 0, 0, 0.2);
}
.event-card {
  text-align: center;
}
</style>

