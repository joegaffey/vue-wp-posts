<template>

  <form @submit.prevent="submitForm">
    <label for="name">Enter WordPress URL:</label>
    <input type="text" id="name" v-model="name" placeholder="" />

    <button type="submit">Submit</button>
  </form>

  <div v-if="submitted" class="post-list">
    <h2>Latest Posts</h2>
    <div v-if="loading">Loading...</div>
    <div v-if="error" class="error">{{ error }}</div>
    <ul v-if="posts.length">
      <li v-for="post in posts" :key="post.id">
        <h3>{{ post.title.rendered }}</h3>
        <p v-html="post.excerpt.rendered"></p>
      </li>
    </ul>
    <div v-if="!loading && posts.length === 0">No posts available.</div>
  </div>
</template>

<script>
  
export default {
  data() {
    return {
      posts: [],
      submitted: false,
      name: null,
      loading: true,
      error: null,
    }
  },
  created() {
    this.fetchPosts()
  },
  methods: {
    submitForm() {
      this.submitted = true;
      this.fetchPosts();
    },
    async fetchPosts() {
      
      let wordpressUrl = this.name;

      if (!wordpressUrl || wordpressUrl.length < 5) {
        this.loading = false;
        return;
      }

      try {
        const response = await fetch(`${wordpressUrl}/wp-json/wp/v2/posts`);
        if (!response.ok) {
          throw new Error(`HTTP error! status: ${response.status}`);
        }
        this.posts = await response.json();
      } catch (err) {
        error = err.message;
    } 
    finally {
      loading = false;
    }
  },
  },
}
</script>

<style scoped>
.post-list {
  font-family: Arial, sans-serif;
}

h2 {
  color: #333;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin-bottom: 20px;
  border-bottom: 1px solid #ddd;
  padding-bottom: 15px;
}

h3 {
  color: #0073e6;
}

.error {
  color: red;
}

a {
  color: #0073e6;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
</style>
