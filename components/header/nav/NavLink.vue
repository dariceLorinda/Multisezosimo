<script>
import NavLinkIntern from "@/components/header/nav/NavLinkIntern.vue";

export default {
  components: {
    NavLinkIntern
  },
  props: {
    navigationLink: Object
  }
}
</script>

<template>
  <a href="#">{{navigationLink.name}}</a>
  <div>
    <ul>
      <li v-for="linkIntern in navigationLink.linkInter">
        <a href="#">{{ linkIntern.name }}</a>
      </li>
    </ul>
  </div>
</template>

<style scoped>

</style>