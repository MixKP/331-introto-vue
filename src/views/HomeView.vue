<script setup lang="ts">
import EventCard from '@/components/EventCard.vue';
import { ref } from 'vue';
import type { Event } from '@/type';

const events = ref<Event[]>([
  {
  id: 5928101,
  category: 'animal welfare',
  title: 'Cat Adoption Day',
  description: 'Find your new feline friend at this event.',
  location: 'Meow Town',
  date: 'January 28, 2002',
  time: '12:00',
  petsAllowed: true,
  organizer: 'Kat Laydee'
  },
  {
  id: 4582797,
  category: 'food',
  title: 'Community Gardening',
  description: 'Join us as we tent to community edible plants.',
  location: 'Flora City',
  date: 'March 14, 2022',
  time: '10:00',
  petsAllowed: true,
  organizer: 'Fern Pollin'
  },
  {
  id: 86419988,
  category: 'sustainability',
  title: 'Beach Cleanup',
  description: 'Help pick up trach along the shore.',
  location: 'Playa Del Carmen',
  date: 'July 22, 2022',
  time: '11:00',
  petsAllowed: false,
  organizer: 'Carey Wales'
  }
]);
</script>

<template>
  <!-- <main>
    <TheWelcome />
  </main> -->
  <div class="home">
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>
