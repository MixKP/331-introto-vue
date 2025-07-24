<script setup lang="ts">
import type { Event } from '@/type';

defineProps<{
  event: Event
}>()
</script>

<template>
  <div class="event-details">
    <div class="category">{{ event.category }}</div>
    <div class="organizer">{{ event.organizer }}</div>
  </div>
</template>

<style scoped>
.event-details {
  text-align: right;
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}

.category,
.organizer {
  font-size: 16px;
  margin: 5px 0;
}
</style>
