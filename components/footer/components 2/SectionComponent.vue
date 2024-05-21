<template>
  <div class="section">
    <div class="highlighted-article">
      <ArticleComponent :article="highlightedArticle" />
    </div>
    <div class="center-images">
      <img v-for="(image, index) in centerImages" :key="index" :src="image" alt="Center Image">
    </div>
    <div class="bottom-articles">
      <ArticleComponent v-for="(article, index) in bottomArticles" :key="index" :article="article" />
    </div>
    <div class="right-articles">
      <ArticleComponent v-for="(article, index) in rightArticles" :key="index" :article="article" />
    </div>
  </div>
</template>

<script>
import ArticleComponent from './ArticleComponent.vue';

export default {
  components: {
    ArticleComponent
  },
  props: {
    highlightedArticle: Object,
    centerImages: Array,
    bottomArticles: Array,
    rightArticles: Array
  }
};
</script>

<style scoped>
.section {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 20px;
  margin-bottom: 40px;
}

.highlighted-article {
  grid-column: span 2;
}

.center-images {
  grid-column: span 2;
  display: flex;
  justify-content: space-between;
}

.center-images img {
  width: 48%;
  height: auto;
}

.bottom-articles {
  grid-column: span 2;
  display: flex;
  justify-content: space-between;
}

.right-articles {
  grid-column: span 1;
  display: flex;
  flex-direction: column;
}
</style>
