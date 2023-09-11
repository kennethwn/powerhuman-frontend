<template>
  <div>
    <h1>{{ post.title }}</h1>
    <p>{{ post.description }}</p>
  </div>
</template>

<script>
  import axios from 'axios'

  export default {
    async asyncData() {
      const post = await axios.get(`https://api.nuxtjs.dev/posts/1`)
      return { post }
    }
  }
</script>
