<script setup lang="ts">

import { ref, onMounted } from 'vue'

// reactive state
const newItem = ref('')
const items = ref([{
    name: 'item1'
},
{
    name: 'item2'
},
{
    name: 'item3'
}])

// functions that mutate state and trigger updates
function add(name: string) {
  items.value.push({
    name
  })
  newItem.value = ''
}

// lifecycle hooks
onMounted(() => {
})

</script>

<template>
<ul class="item-list">
    <li v-for="item in items" :key="item.name">
        {{item.name}}
    </li>

</ul>
<div class="new-item-actions">
<input type="text" v-model="newItem">
  <button @click="add(newItem)">Add item</button>
</div>
</template>

<style scoped>
.item-list {
    margin-bottom: 10px;
}
.new-item-actions {
    display: flex;
    flex-direction: column;
    justify-content: center;
}
button {
  font-weight: 500;
  font-size: 1rem;
  background-color: hsla(160, 100%, 37%, 1);
  color: white;
  padding: 10px;
  cursor: pointer;
  border: 0;
  margin-top: 10px;   
}
</style>
