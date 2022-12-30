<script setup>
import { ref } from 'vue'

defineProps({
  title: {
    type: String,
    default: '',
  },
})

const emit = defineEmits(['on-click'])

const names = 'Antony'
const textInput = ref('')

function handleClickHello(value) {
  emit('on-click', value)
}
</script>

<template>
  <div>
    <h3>{{ title }}</h3>
    <div>
      <div>Hello World!</div>
      <button @click="() => handleClickHello(textInput)">click!</button>
    </div>
    <div>Name: {{ names }}</div>
    <input
      v-model="textInput"
      class="inputTxt"
      type="text"
      placeholder="Type here..."
    />
    <div>input: {{ textInput }}</div>
    <slot></slot>
  </div>
</template>

<style scoped>
.inputTxt {
  margin: 15px 0;
  padding: 10px 15px;
  border: 2px solid lightslategray;
  border-radius: 3px;
}
</style>
