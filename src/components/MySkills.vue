<template>
  <div class="skills">
    <div class="app-container">
      <h2>Skills</h2>
      <div class="skills-wrapper">
        <div class="skills__item"  v-for="icon in icons"  :key="icon.id">
          <i :class="icon.icon"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
data() {
  return {
    icons: [
      { id: 1, icon: "devicon-javascript-plain" },
      { id: 2, icon: "devicon-jquery-plain" },
      { id: 3, icon: "devicon-react-original" },
      { id: 4, icon: "devicon-html5-plain" },
      { id: 4, icon: "devicon-css3-plain" },
      { id: 4, icon: "devicon-redux-original" },
      { id: 4, icon: "devicon-sass-original" },
      { id: 4, icon: "devicon-vuejs-plain" },
      { id: 4, icon: "devicon-npm-original-wordmark" },
      { id: 4, icon: "devicon-git-plain" },
      { id: 4, icon: "devicon-figma-plain" },
    ],
  }
}
}
</script>

<style lang="scss" scoped>
.skills {
  position: relative;
  z-index: 2;
  background-color: dimgrey;
  &-wrapper {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    width: 100%;
  }
  &__item {
    text-align: center;
    width: 100%;
    max-width: 25%;
    font-size: 100px;
    border: 1px solid white;
    transition: all .5s ease-in-out;
    i {
      color: white;
      transition: all .5s ease-in-out;
    }
    &:hover {
      background-color: white;
      & i {
        color: black;
      }
    }
  }
}
</style>