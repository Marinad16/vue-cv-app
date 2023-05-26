<template>
  <div class="app-container">
    <h2 class="app-title">My Projects</h2>
    <p>This is an example of a portfolio gallery. It has some simple hover transitions and is pretty rad.</p>
    <div class="projects-gallery">
      <div class="projects__item-wrap" v-for="project in projects" :key="project.id">
        <div class="projects__item" >
          <div class="projects__item-img">
            <img
                :src="getImagePath(project.image)"
                :alt="project.title"/>
          </div>
          <div class="projects__item-overlay">
            <h3 class="projects__item-title">{{project.title}}</h3>
            <p class="projects__item-about">{{project.about}}</p>
            <p class="projects__item-about">{{project.technologies}}</p>
            <a target="_blank" class="projects__item-link" :href="project.link">Go to website</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: "Perfect Baby Fit",
          about: "React project for choosing the perfect size of clothes for a child. Develop complicated filters with different params, multilingual, pagination",
          link: "#",
          technologies: "React, React Router, Redux, Redux Saga, i18n, SCSS, REST API, Swagger, Figma",
          image: "baby-fit.png"
        },
        {
          id: 2,
          title: "Onlime store",
          about: "Online store of digital equipment and gadgets. Develop products compare table, basket, theme change",
          link: "#",
          technologies: "Laravel blades, jQuery, SCSS, Alpine.js, AJAX.",
          image: "onlime.png"
        },
        {
          id: 3,
          title: "Svitanok juice",
          about: "Landing for juice company with cute animation.",
          link: "http://www.svitanok-juice.com.ua/",
          technologies: "Laravel blades, jQuery, SCSS.",
          image: "svitanok.png"
        },
        {
          id: 4,
          title: "Code of the nation",
          about: "Website for the charitable fund Code of the nation.",
          link: "https://code-of-nation.org.ua/",
          technologies: "Laravel blades, jQuery, SCSS, AJAX, Leaflet.js.",
          image: "kod-of-nation.png"
        },
        {
          id: 5,
          title: "Victory harvest",
          about: "Website for the charitable fund Victory harvest. ",
          link: "https://victoryharvest.com.ua/",
          technologies: "Laravel blades, jQuery, SCSS, AJAX.",
          image: "harvest.png"
        },
        {
          id: 5,
          title: "Download Center",
          about: "Download Center for IEC Telecom company.",
          link: "https://downloadcenter.iec-telecom.com/",
          technologies: "Laravel blades, jQuery, SCSS, AJAX.",
          image: "download-center.png"
        },
      ],
    }
  },
  methods: {
    getImagePath(image) {
      return require(`@/assets/images/${image}`);
    }
  }
}
</script>

<style lang="scss" scoped>
.projects-gallery {
  width: calc(100% + 60px);
  margin-left: -30px;
  display: flex;
  flex-wrap: wrap;
}

.projects__item {
  position: relative;
  height: 300px;
  border-radius: 10px;
  box-shadow: 0 25px 50px rgba(0, 0, 0, .5);
  overflow: hidden;
  transition: all .4s ease;
  width: 100%;

  &-wrap {
    flex: 0 0 50%;
    max-width: 50%;
    width: 100%;
    padding: 30px;
  }
  &-img {
    width: 100%;
    height: 300px;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  &-overlay {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    z-index: 10;
    display: flex;
    justify-content: space-between;
    flex-direction: column;

    &:after {
      content: '';
      width: 100%;
      border-radius: 10px;
      height: 100%;
      background-color: #202020;
      opacity: 0.2;
      position: absolute;
      top: 0;
      z-index: -10;
      left: 0;
      transition: all .3s ease;
    }
  }

  &-title {
    position: relative;
    top: -200px;
    margin-top: 30px;
    font-size: 2.25rem;
    font-family: 'Oswald';
    font-weight: 100;
    color: white;
    text-align: center;
    letter-spacing: 5px;
    transition: all .5s cubic-bezier(.3, 0, 0, 1.3);
  }

  &-about {
    margin-top: 1rem;
    text-align: center;
    padding: 0 10px;
    position: relative;
    top: -230px;
    font-size: 1rem;
    font-family: 'Oswald';
    font-weight: 100;
    color: white;
    letter-spacing: 5px;
    transition: all .5s cubic-bezier(.3, 0, 0, 1.3);
  }

  &-link {
    position: relative;
    display: block;
    width: 60%;
    top: 200px;
    padding: 10px;
    margin: 30px auto;
    font-family: 'Oswald';
    color: white;
    letter-spacing: 3px;
    text-decoration: none;
    text-align: center;
    border: 2px solid white;
    border-radius: 3px;
    font-size: 1.25em;
    transition: all .5s cubic-bezier(.3, 0, 0, 1.3);

    &:hover {
      background-color: white;
      color: #202020;
    }
  }

  &:hover {
    .projects__item-title {
      top: 0;
    }

    .projects__item-link {
      top: 0;
    }

    .projects__item-about {
      top: 0;
    }

    .projects__item-overlay:after {
      opacity: .85;
    }
  }
}

</style>