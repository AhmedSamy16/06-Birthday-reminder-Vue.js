
<template>
  <main>
    <section class="container">
      <h3>{{ users.data.length }} Birthday Today</h3>
      <List :data="users.data" />
      <button @click="clearAll">
        Clear All
      </button>
    </section>
  </main>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import List from './List.vue';
import data from './data';

const users = ref({ data })

const clearAll = () => {
  users.value.data = []
}
</script>