<template>
    <main-banner/>
    <my-skills/>
    <my-projects/>
</template>

<script>
import MainBanner from "@/components/MainBanner";
import MySkills from "@/components/MySkills";
import MyProjects from "@/components/MyProjects";
export default {
  name: 'App',
  components: {
    MySkills,
    MainBanner,
    MyProjects,
  }
}
</script>
<style lang="sass">
*
  margin: 0
  padding: 0
  box-sizing: border-box
html
  height: 100%
body
  margin: 0
  font-family: 'Roboto Mono', monospace
  height: 100%
  overflow-x: hidden

.app-container
  width: 100%
  max-width: 1320px
  padding: 20px
  margin: 0 auto
</style>

