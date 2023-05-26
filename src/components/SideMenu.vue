<!--<template>-->
<!--  <div id="side-menu">-->
<!--    <div class="uic-sidenav">-->
<!--      <h2 @click.stop="menuSelect(null)">HEADING</h2>-->
<!--      <a href="#"-->
<!--         :key="index"-->
<!--         v-for="(page, index) of pages"-->
<!--         :class="{ active: page.selected }"-->
<!--         @click.stop="menuSelect(index)"-->
<!--      >-->
<!--        {{ page.link }}-->
<!--      </a>-->
<!--    </div>-->

<!--    <div class="uic-body">-->
<!--      <div class="uic-content">-->
<!--        <h1>{{ selectedPage && selectedPage.title }}</h1>-->
<!--      </div>-->
<!--    </div>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  el: '#side-menu',-->
<!--  computed: {-->
<!--    selectedPage: function() {-->
<!--      const selected = this.pages.filter(function(page) {-->
<!--        return page.selected;-->
<!--      });-->
<!--      return selected.length > 0 ? selected[0] : null;-->
<!--    }-->
<!--  },-->
<!--  data: function() {-->
<!--    return {-->
<!--      pages: [{-->
<!--        link: 'About',-->
<!--        selected: false,-->
<!--        title: 'About the Company',-->
<!--      }, {-->
<!--        link: 'Services',-->
<!--        selected: false,-->
<!--        title: 'Services Offered'-->
<!--      }, {-->
<!--        link: 'Clients',-->
<!--        selected: false,-->
<!--        title: 'Our Clients'-->
<!--      }, {-->
<!--        link: 'Contact',-->
<!--        selected: false,-->
<!--        title: 'Contact Us'-->
<!--      }]-->
<!--    }-->
<!--  },-->
<!--  methods: {-->
<!--    menuSelect: function(index) {-->
<!--      this.pages = this.pages.map(function(page) {-->
<!--        page.selected = false;-->
<!--        return page;-->
<!--      });-->
<!--      if (index !== null) {-->
<!--        this.pages[index].selected = true;-->
<!--      }-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->
<!--.uic-sidenav {-->
<!--  width: 150px;-->
<!--  position: fixed;-->
<!--  top: 0;-->
<!--  left: 0;-->
<!--  bottom: 0;-->
<!--  border-right: 1px solid #F4511E;-->
<!--}-->

<!--.uic-sidenav h2 {-->
<!--  display: block;-->
<!--}-->

<!--.uic-sidenav .active {-->
<!--  background-color: white;-->
<!--  color: #F4511E;-->
<!--}-->

<!--.uic-sidenav a {-->
<!--  display: block;-->
<!--}-->

<!--.uic-body {-->
<!--  display: flex;-->
<!--  margin-left: 150px;-->
<!--}-->

<!--.uic-content {-->
<!--  margin: auto;-->
<!--  text-align: center;-->
<!--}-->

<!--/* STYLES */-->
<!--body {-->
<!--  font-family: "Work Sans", "Helvetica", "Tahoma", "Geneva", "Arial", sans-serif;-->
<!--}-->

<!--.uic-sidenav {-->
<!--  z-index: 1;-->
<!--  background-color: #F4511E;-->
<!--}-->

<!--.uic-sidenav h2 {-->
<!--  padding: 8px 8px 8px 8px;-->
<!--  margin: 0;-->
<!--  text-decoration: none;-->
<!--  color: white;-->
<!--}-->

<!--.uic-sidenav a {-->
<!--  padding: 8px 8px 8px 32px;-->
<!--  text-decoration: none;-->
<!--  font-size: 20px;-->
<!--  color: white;-->
<!--}-->
<!--</style>-->