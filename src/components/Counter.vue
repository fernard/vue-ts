<script setup lang="ts">

import { ref, onMounted } from 'vue'

// reactive state
const count = ref(0)

// functions that mutate state and trigger updates
function increment() {
  count.value++
}

// lifecycle hooks
onMounted(() => {
  console.log(`The initial count is ${count.value}.`)
})

</script>

<template>
<div>
    <button @click="increment">Count is: {{ count }}</button>
</div>
</template>

<style scoped>
button {
  font-weight: 500;
  font-size: 1rem;
  background-color: hsla(160, 100%, 37%, 1);
  color: white;
  padding: 10px;
  cursor: pointer;
  border: 0;
}
</style>
