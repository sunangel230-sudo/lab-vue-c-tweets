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
    <ProfileImage :image="tweet.user.image" />

    <div class="body">
      <div class="top">
        <User :userData="tweet.user" />
        <Timestamp :time="tweet.timestamp" />
      </div>

      <Message :message="tweet.message" />
      <Actions />
    </div>
  </div>
</template>

<style scoped>
.tweet {
  display: flex;
  padding: 12px;
  border-bottom: 1px solid #e6ecf0;
}

.body {
  margin-left: 10px;
  flex: 1;
}

.top {
  display: flex;
  gap: 6px;
  align-items: center;
  margin-bottom: 4px;
}
</style>