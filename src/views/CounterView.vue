<script setup lang="ts">
import Counter from '@/components/Counter.vue'

</script>

<template>
  <div class="wrapper">
    <Counter />
  </div>
</template>

<style>
.wrapper {
  display: flex;
  align-items: center;
  
}

.wrapper > * {
  margin-right: 5px;
}
</style>

