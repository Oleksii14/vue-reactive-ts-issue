<script setup lang="ts">
import { computed, reactive, ref } from 'vue';

interface Form {
  a: number
  b: number
}

const counter = ref(1)

const form = reactive<Form>({
  a: 1,
  // ts error
  b: counter
})

// or

// const form = reactive<Form>({
//   a: 1,
//   b: computed(() => counter.value + 1)
// })
</script>

<template>
  {{ form }}  
</template>
