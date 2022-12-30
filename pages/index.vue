<template>
  <HelloWorld title="Welcome to Nuxt 3" @on-click="handleClick">
    HelloChild
  </HelloWorld>
</template>
<script lang="ts" setup>
const handleClick = (value: string) => {
  console.log('>> emit from HelloWorld: ', value)
}
</script>
