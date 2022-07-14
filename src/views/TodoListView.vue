<script setup lang="ts">
import TodoList from '@/components/TodoList.vue'
</script>

<template>
  <div class="wrapper">

    <TodoList/>
    </div>
</template>


<style>
.wrapper {
  align-items: flex-start;
  display: flex;
  flex-direction: column;
}
</style>
