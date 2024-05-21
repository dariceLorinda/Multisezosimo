<script>
  import NavLink from "@/components/header/nav/NavLink.vue";
  export default {
    components: {NavLink},
    data() {
      return {
        navigationLinkList: [
          {
            id: 1,
            name: "Latest",
            url: "#",
            linkInter: [
              {
                id: 11,
                name: "A",
                url: "#"
              },
              {
                id: 12,
                name: "B",
                url: "#"
              },
              {
                id: 13,
                name: "C",
                url: "#"
              }
            ]
          },
          {
            id: 2,
            name: "Local News",
            url: "#",
            linkInter: [
              {
                id: 21,
                name: "A",
                url: "#"
              },
              {
                id: 22,
                name: "B",
                url: "#"
              },
              {
                id: 23,
                name: "C",
                url: "#"
              }
            ]
          },
          {
            id: 3,
            name: "Live",
            url: "#",
            linkInter: [
              {
                id: 31,
                name: "A",
                url: "#"
              },
              {
                id: 32,
                name: "B",
                url: "#"
              },
              {
                id: 33,
                name: "C",
                url: "#"
              }
            ]
          },
          {
            id: 4,
            name: "Shows",
            url: "#",
            linkInter: [
              {
                id: 41,
                name: "A",
                url: "#"
              },
              {
                id: 42,
                name: "B",
                url: "#"
              },
              {
                id: 43,
                name: "C",
                url: "#"
              }
            ]
          },
          {
            id: 5,
            name: "...",
            url: "#",
            linkInter: [
              {
                id: 51,
                name: "A",
                url: "#"
              },
              {
                id: 52,
                name: "B",
                url: "#"
              },
              {
                id: 53,
                name: "C",
                url: "#"
              }
            ]
          }
        ]
      }
    }
  }
</script>

<template>
  <nav>
    <ul>
      <li v-for="navLink in navigationLinkList">
        <nav-link :navigationLink="navLink"></nav-link>
      </li>
    </ul>
  </nav>
</template>

<style scoped>

</style>