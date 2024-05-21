<template>
  <div class="article">
    <h3>{{ article.title }}</h3>
    <p v-if="article.preview">{{ article.preview }}</p>
    <small>{{ formatDate(article.date) }}</small>
    <img v-if="article.image && article.showImage" :src="article.image" :alt="article.title">
  </div>
</template>

<script>
export default {
  props: {
    article: Object
  },
  methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric', hour: '2-digit', minute: '2-digit' };
      return new Date(date).toLocaleDateString(undefined, options);
    }
  }
};
</script>

<style scoped>
.article {
  margin-bottom: 20px;
}

.article img {
  width: 100%;
  height: auto;
  margin-top: 10px;
}
</style>
