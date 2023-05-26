<template>
  <!--  <side-menu/>-->
  <main-banner/>
  <my-skills/>
  <my-projects/>
</template>

<script>
import MainBanner from "@/components/MainBanner";
import MySkills from "@/components/MySkills";
import MyProjects from "@/components/MyProjects";
// import SideMenu from "@/components/SideMenu";

export default {
  name: 'App',
  components: {
    MySkills,
    MainBanner,
    MyProjects,
    // SideMenu,
  }
}
</script>
<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  height: 100%;
}

body {
  margin: 0;
  font-family: 'Roboto Mono', monospace;
  height: 100%;
  overflow-x: hidden;
}

.app-container {
  width: 100%;
  max-width: 1320px;
  padding: 20px;
  margin: 0 auto;
}

.app-title {
  text-align: center;
  font-size: 48px;
  display: block;

  &::after {
    content: "";
    background: #f35b04;
    height: 2px;
    width: 100px;
    display: block;
    text-align: center;
    margin: 0 auto;
    margin-bottom: 20px;
    margin-top: 10px;
  }
}
</style>

