<script setup lang="ts">
const props = defineProps<{
  initial: number
}>()

const { count, inc, dec } = useCounter(props.initial)
</script>

<template>
  <div class="space-y-2.5 space-x-5">
    <span>{{ count }}</span>
    <button class="inc" @click="inc()">+</button>
    <button class="dec" @click="dec()">-</button>
  </div>
</template>
