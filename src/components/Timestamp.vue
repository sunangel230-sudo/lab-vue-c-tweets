Timestamp.vue
<script setup>
defineProps({
  time: String
})
</script>

<template>
  <span class="timestamp"> · {{ time }}</span>
</template>
