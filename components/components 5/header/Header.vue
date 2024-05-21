<script setup>

import ElementSearch from "@/components/header/ElementSearch.vue";
import NavElement from "@/components/header/nav/NavElement.vue";
</script>

<template>
  <div>
    <NavElement />
  </div>
  <div>
    <a href="#">
      <img class="header-logo" src="../../assets/CBS%20News.svg" alt="CBS News Logo">
    </a>
  </div>
  <div>
    <ElementSearch />
  </div>

</template>

<style scoped>
.header-logo {
  width: 150px;
}
</style>