<script setup>
import { ref } from 'vue'
import Tweet from './components/Tweet.vue'

const tweets = [
  {
    id: 1,
    user: {
      name: "Ironhack",
      handle: "@ironhack",
      image: "https://i.imgur.com/9yw1Fyw.jpg"
    },
    timestamp: "Nov 30, 2020",
    message:
      "On December 7th, we will be hosting a #webinar that will introduce you to #SQL! Are you ready? 🚀"
  },
  {
    id: 2,
    user: {
      name: "Thoughts of Dog",
      handle: "dog_feelings",
      image: "https://i.imgur.com/b0EdHVV.jpg",
    },
    timestamp: "1h ago",
    message:
      "the human likes to say. that i live here rent free. but i would argue. this housing accommodation. is my payment. for a lifetime of love. and excellent company"
  },
  {
    id: 3,
    user: {
      name: "Thoughts of Dog",
      handle: "dog_feelings",
      image: "https://i.imgur.com/b0EdHVV.jpg",
    },
    timestamp: "2h ago",
    message:
      "sometimes. the human presses their noggin against mine. to figure out what i'm thinking. so i just think really hard. about how much i love them. and hope they figure it out"
  },
  {
    id: 4,
    user: {
      name: "Thoughts of Dog",
      handle: "dog_feelings",
      image: "https://i.imgur.com/b0EdHVV.jpg",
    },
    timestamp: "3h ago",
    message: `here is what. i plan to accomplish today:

2. bark loudly. but at nothing
7. lose my ball under the couch
7b. politely ask the human. to get my ball
3. immediately lose it again. under the same couch
4. big nap. you have worked hard
2. repeat`
  }
]
</script>

<template>
  <div class="app">
    <Tweet
      v-for="tweet in tweets"
      :key="tweet.id"
      :tweet="tweet"
    />
  </div>
</template>

<style>
body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #f5f8fa;
}

/* App container */
.app {
  max-width: 650px;
  margin: 0 auto;
  padding: 20px;
  background: white;
  border-left: 1px solid #e6ecf0;
  border-right: 1px solid #e6ecf0;
}

/* Tweet layout */
.tweet {
  margin: 0 auto;
  padding: 10px;
  border-bottom: 1px solid #e6ecf0;
  display: flex;
  font-size: 1.1rem;
  line-height: 18px;
}

.body {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.top {
  display: flex;
  line-height: 1.4rem;
  align-items: center;
}

/* Profile */
.profile {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-right: 10px;
}

/* Text styles */
.name {
  font-weight: bold;
  margin-right: 0.3em;
}

.handle {
  color: #536471;
  margin: 0 3px;
}

.timestamp {
  color: #536471;
  font-size: 1rem;
}

.timestamp::before {
  content: "·";
  padding: 0 0.3em;
}

/* Message */
.message {
  text-align: left;
  font-weight: 400;
  line-height: 1.6rem;
  white-space: pre-wrap;
  word-break: break-word;
}

/* Actions */
.actions {
  padding: 5px;
  width: 360px;
  display: flex;
  justify-content: space-between;
  color: #536471;
}
</style>