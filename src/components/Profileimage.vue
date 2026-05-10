<script setup>
defineProps({
  image: String
})
</script>

<template>
  <img :src="image" class="profile" alt="profile" />
</template>