<script>
  import ArticleSection from "@/components/section/article/ArticleSection.vue";

  export default {
    components: {ArticleSection},
    data() {
      return {
        articleList: [
          {
            id: 1,
            principal: true,
            title: "Article Id 1",
            content: "Article Id 1 Content",
            date: "UPDATED 33M AGO"
          }
        ]
      }
    }
  }
</script>

<template>
  <section>
    <div v-for="articleElement in articleList">
      <article-section :article-section-element="articleElement"></article-section>
    </div>
  </section>
</template>

<style scoped>

</style>