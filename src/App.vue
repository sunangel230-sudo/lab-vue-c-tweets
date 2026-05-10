<template>
  <div class="app">
    <Tweet
      v-for="tweet in tweets"
      :key="tweet.id"
      :tweet="tweet"
    />
  </div>
</template>

<script setup>
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
      "On December 7th, we will be hosting a #webinar that will introduce you to #SQL! 🚀"
  },
  {
    id: 2,
    user: {
      name: "Thoughts of Dog",
      handle: "dog_feelings",
      image: "https://i.imgur.com/b0EdHVV.jpg"
    },
    timestamp: "1h ago",
    message:
      "the human likes to say that i live here rent free. but i would argue this housing is my payment for love."
  },
  {
    id: 3,
    user: {
      name: "Thoughts of Dog",
      handle: "dog_feelings",
      image: "https://i.imgur.com/b0EdHVV.jpg"
    },
    timestamp: "2h ago",
    message:
      "sometimes the human presses their head against mine to figure out what I’m thinking."
  },
  {
    id: 4,
    user: {
      name: "Thoughts of Dog",
      handle: "dog_feelings",
      image: "https://i.imgur.com/b0EdHVV.jpg"
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

<style>
body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
    "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.app {
  text-align: center;
  padding: 20px;
}

.app-logo {
  height: 40vmin;
  pointer-events: none;
}

@media (prefers-reduced-motion: no-preference) {
  .app-logo {
    animation: App-logo-spin infinite 20s linear;
  }
}

.app-header {
  background-color: #282c34;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: calc(10px + 2vmin);
  color: white;
}

.app-link {
  color: #61dafb;
}

@keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.tweet {
  margin: 0 auto;
  min-width: 480px;
  max-width: 640px;
  min-height: 80px;
  padding: 10px;
  border: 1px solid #ccc;
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
}

.more {
  margin-left: 20px;
}

.profile {
  width: 50px;
  height: 50px;
  border-radius: 50px;
  margin-right: 10px;
}

.name {
  font-weight: bold;
  margin-bottom: 0.5em;
  margin-right: 0.3em;
}

.handle {
  color: #536471;
  margin-left: 3px;
  margin-right: 3px;
}

.timestamp {
  color: #536471;
  font-size: 1.1rem;
}

.timestamp::before {
  content: "·";
  padding-right: 0.3em;
  font-size: 1.1rem;
  font-weight: 600;
}

.message {
  text-align: left;
  font-stretch: 100%;
  font-weight: 400;
  line-height: 1.6rem;
  overflow-wrap: break-word;
  white-space: pre-wrap;
}

.actions {
  padding: 5px 5px;
  width: 360px;
  display: flex;
  justify-content: space-between;
  color: #536471;
}
</style>