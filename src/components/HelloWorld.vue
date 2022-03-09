<script setup lang="ts">
import { useCounterStore } from '@/stores/counter';
import { storeToRefs } from 'pinia'

const store = useCounterStore() 

const {counter, doubleCount} = storeToRefs(store)

const {reset} = store

</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ counter }}</h1>
    <h3>
      This number above, comes from a pinia store
    </h3>
    <button @click="reset">Reset</button>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
