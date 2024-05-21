<template>
  <header class="header">
    <nav class="nav-left">
      <div class="nav-item" v-for="item in navigationLinkList" :key="item.name">
        <a href="#">{{ item.name }}</a>
        <div class="dropdown" v-if="item.linkInter">
          <div class="dropdown-column" v-for="(col, index) in getColumns(item.linkInter)" :key="index">
            <a v-for="link in col" :key="link.name" href="#">{{ link.name }}</a>
          </div>
        </div>
      </div>
    </nav>
    <div class="site-icon">
      <a href="#">
        <img src="../assets/CBS%20News.svg" alt="CBS News Logo">
      </a>
    </div>
    <div class="search-right">
      <ElementSearch />
    </div>
  </header>
</template>

<script>
import ElementSearch from "@/components/ElementSearchComponent.vue";

export default {
  components: {ElementSearch},
  data() {
    return {
      navItems: [
        { text: 'Home', dropdown: null },
        { text: 'About', dropdown: ['Team', 'History', 'Contact'] },
        { text: 'Services', dropdown: ['Consulting', 'Development', 'Design'] },
        { text: 'Products', dropdown: ['Software', 'Hardware', 'Accessories'] }
      ],
      navigationLinkList: [
        {
          id: 1, name: "Latest", url: "#",
          linkInter: [
            {id: 101, name: "U.S.", url: "#"},
            {id: 102, name: "World", url: "#"},
            {id: 103, name: "Politics", url: "#"},
            {id: 104, name: "Entertainment", url: "#"},
            {id: 105, name: "HealthWatch", url: "#"},
            {id: 106, name: "MoneyWatch", url: "#"},
            {id: 107, name: "Investigations", url: "#"},
            {id: 108, name: "Crime", url: "#"},
            {id: 109, name: "Space", url: "#"},
            {id: 110, name: "Sports", url: "#"}
          ]
        },
        {
          id: 2, name: "Local News", url: "#",
          linkInter: [
            {id: 201, name: "Baltimore", url: "#"},
            {id: 202, name: "Bay Area", url: "#"},
            {id: 203, name: "Boston", url: "#"},
            {id: 204, name: "Chicago", url: "#"},
            {id: 205, name: "Colorado", url: "#"},
            {id: 206, name: "Detroit", url: "#"},
            {id: 207, name: "Los Angeles", url: "#"},
            {id: 208, name: "Miami", url: "#"},
            {id: 209, name: "Minnesota", url: "#"},
            {id: 210, name: "New York", url: "#"},
            {id: 211, name: "Philadelphia", url: "#"},
            {id: 212, name: "Pittsburgh", url: "#"},
            {id: 213, name: "Sacramento", url: "#"},
            {id: 214, name: "Texas", url: "#"}
          ]
        },
        {
          id: 3, name: "Live", url: "#",
          linkInter: [
            {id: 301, name: "CBS News 24/7", url: "#"},
            {id: 302, name: "Baltimore", url: "#"},
            {id: 303, name: "Bay Area", url: "#"},
            {id: 304, name: "Boston", url: "#"},
            {id: 305, name: "Chicago", url: "#"},
            {id: 306, name: "Colorado", url: "#"},
            {id: 307, name: "Detroit", url: "#"},
            {id: 308, name: "Los Angeles", url: "#"},
            {id: 309, name: "Miami", url: "#"},
            {id: 310, name: "Minnesota", url: "#"},
            {id: 311, name: "New York", url: "#"},
            {id: 312, name: "Philadelphia", url: "#"},
            {id: 313, name: "Pittsburgh", url: "#"},
            {id: 314, name: "Sacramento", url: "#"},
            {id: 315, name: "Texas", url: "#"}
          ]
        },
        {
          id: 4, name: "Shows", url: "#",
          linkInter: [
            {id: 401, name: "48 Hours", url: "#"},
            {id: 402, name: "60 Minutes", url: "#"},
            {id: 403, name: "America Decides", url: "#"},
            {id: 404, name: "CBS Evening News", url: "#"},
            {id: 405, name: "CBS Mornings", url: "#"},
            {id: 406, name: "CBS News Eye on America", url: "#"},
            {id: 407, name: "CBS News Mornings", url: "#"},
            {id: 408, name: "CBS Reports", url: "#"},
            {id: 409, name: "CBS Saturday Morning", url: "#"},
            {id: 410, name: "The Daily Report", url: "#"},
            {id: 411, name: "The Dish", url: "#"},
            {id: 412, name: "Face the Nation", url: "#"},
            {id: 413, name: "Here Comes the Sun", url: "#"},
            {id: 414, name: "Person to Person", url: "#"},
            {id: 415, name: "Sunday Morning", url: "#"},
            {id: 416, name: "The Takeout", url: "#"},
            {id: 417, name: "The Uplift", url: "#"},
            {id: 418, name: "Weekender", url: "#"},
          ]
        },
        {
          // id: 5, name: "<svg viewBox=\"0 0 16 16\" class=\"site-nav__item-icon site-nav__item-icon--type-more\" aria-hidden=\"true\"><use xlink:href=\"#icon-nav-more\"></use></svg>", url: "#",
          id: 5, name: "...", url: "#",
          linkInter: [
            {id: 501, name: "CBS News Investigates", url: "#"},
            {id: 502, name: "Photos", url: "#"},
            {id: 503, name: "Podcasts", url: "#"},
            {id: 504, name: "In Depth", url: "#"},
            {id: 505, name: "Newsletters", url: "#"},
            {id: 506, name: "Download Our App", url: "#"},
            {id: 507, name: "CBS News Team", url: "#"},
            {id: 508, name: "Executive Team", url: "#"},
            {id: 509, name: "Paramount Shop", url: "#"},
            {id: 510, name: "Paramount+", url: "#"},
            {id: 511, name: "Join Our Talent Community", url: "#"},
            {id: 512, name: "RSS Feeds", url: "#"},
            {id: 513, name: "A Moment With...", url: "#"},
            {id: 514, name: "Innovators &amp; Disruptors", url: "#"}
          ]
        }
      ]
    };
  },
  methods: {
    getColumns(items) {
      const half = Math.ceil(items.length / 2);
      return [items.slice(0, half), items.slice(half)];
    }
  }
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  /*background-color: #333;*/
  color: black;
}

.nav-left,
.site-icon,
.search-right {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-left {
  justify-content: flex-start;
}

.site-icon {
  justify-content: center;
}

.search-right {
  justify-content: flex-end;
}

.nav-item {
  position: relative;
  margin-right: 20px;
}

.nav-item a {
  /*color: white;*/
  text-decoration: none;
  padding: 10px;
  display: block;
}

.nav-item .dropdown {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  /*background-color: #444;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);*/
  padding: 10px;

}

.nav-item .dropdown-column {
  display: flex;
  flex-direction: column;
  margin-right: 20px;
}

.nav-item .dropdown a {
  padding: 8px 16px;
  white-space: nowrap;
}

.nav-item:hover .dropdown {
  display: flex;
}

.site-icon img {
  height: 40px;
}

.search-right {
  display: flex;
  align-items: center;
}

.search-right input {
  padding: 5px;
  margin-right: 5px;
  border-radius: 4px;
  border: 1px solid;
}

.search-right button {
  padding: 5px 10px;
  border: none;
  background-color: white;
  color: black;
  border-radius: 4px;
  cursor: pointer;
}

</style>
