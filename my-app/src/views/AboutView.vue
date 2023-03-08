<script setup lang="ts">
import {ref} from 'vue';
import type {VDataTableHeader} from '@gits-id/table';

const states = ['active', 'inactive'];

const items = [...Array(50)].map((_, index) => ({
  index,
  name: `User-${index}`,
  email: `user-${index}@example.com`,
  age: index + 1 * 10,
  state: states[Math.floor(Math.random() * states.length)],
}));

const headers = ref<VDataTableHeader[]>([
  {
    value: 'index',
    text: 'ID',
  },
  {
    value: 'name',
    text: 'Name',
  },
  {
    value: 'email',
    text: 'Email',
  },
]);
</script>

<template>
  <!-- VDataTable is registered globally -->
  <VDataTable striped hover flat bordered dense :items="items" :headers="headers" />
  <VLogo />
</template>

