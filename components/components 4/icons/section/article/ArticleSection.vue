<script>
  export default {
    props: {
      articleSectionElement: Object
    }
  }
</script>

<template>
  <article>
    <a href="#">
      <span>
        <img src="../../../assets/cbsnews.jpg" alt="image" layout="responsive" height="360" width="640">
      </span>
      <div>
        <h4>Bla bla titre h4</h4>
        <p>Content</p>
        <ul>
          <li>element 1</li>
          <li>element 2</li>
        </ul>
      </div>
    </a>
  </article>
</template>

<style scoped>

</style>