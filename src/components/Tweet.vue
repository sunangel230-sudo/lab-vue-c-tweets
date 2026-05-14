<script setup>
import ProfileImage from './ProfileImage.vue'
import User from './User.vue'
import Timestamp from './Timestamp.vue'
import Message from './Message.vue'
import Actions from './Actions.vue'

defineProps({
  tweet: Object
})
</script>

<template>
  <div class="tweet">
    <!-- Profile Image -->
    <ProfileImage :image="tweet.user.image" />

    <div class="body">
      <div class="top">
        <!-- User info -->
        <User :userData="tweet.user" />

        <!-- Timestamp -->
        <Timestamp :time="tweet.timestamp" />
      </div>

      <!-- Message -->
      <Message :message="tweet.message" />

      <!-- Actions (no props) -->
      <Actions />
    </div>

    <!-- optional menu icon -->
    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42B983;
}
</style>
