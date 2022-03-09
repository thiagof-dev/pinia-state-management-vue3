<script setup lang="ts">
import {ref} from 'vue'
import { useCounterStore } from '@/stores/counter';
import { storeToRefs } from 'pinia'

const store = useCounterStore() 

const {counter, doubleCount} = storeToRefs(store)

const {increment} = store

</script>

<template>
<h1>Count: {{counter}}</h1>
<h2>Double count: {{doubleCount}}</h2>
<button @click="increment"> Add + 1</button>
<br>
<button>Resset</button>
</template>
