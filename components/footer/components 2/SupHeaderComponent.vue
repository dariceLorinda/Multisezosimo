<script>
export default {
  data() {
    return {
      linkList: [
        {id: 1, name: "U.S", url: "#"},
        {id: 2, name: "World", url: "#"},
        {id: 3, name: "Politics", url: "#"},
        {id: 4, name: "HealthWatch", url: "#"},
        {id: 5, name: "MoneyWatch", url: "#"},
        {id: 6, name: "Entertainment", url: "#"},
        {id: 7, name: "Crime", url: "#"},
        {id: 8, name: "Sports", url: "#"},
        {id: 9, name: "Essentials", url: "#"}
      ]
    }
  }
}
</script>

<template>
  <div class="sup-header">
    <url>
      <li v-for="linkElement in linkList">
        <a href="#">{{linkElement.name}}</a>
      </li>
    </url>
  </div>
</template>

<style scoped>

.sup-header {
  border-top: 1px solid gray;
  border-bottom: 1px solid gray;
  display: flex;
  justify-content: left;
  list-style: none;
}

.sup-header li {
  display: inline;
  margin-right: 10px;
}

.sup-header a {
  text-decoration: none;
}

.sup-header a:hover {
  text-decoration: underline;
}

</style>