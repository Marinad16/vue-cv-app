<template>
  <div class="app-container">
    <h2>My Projects</h2>
    <p>This is an example of a portfolio gallery. It has some simple hover transitions and is pretty rad.</p>
    <div class="projects-gallery">
      <div class="projects__item-wrap">
        <div class="projects__item">
          <div class="projects__item-img">
            <img
                src="https://picsum.photos/200/300"
                alt=""/>
          </div>
          <div class="projects__item-overlay">
            <h3 class="projects__item-title">Developing Hexxis</h3>
            <p class="projects__item-about">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae commodi
              consequatur cumque distinctio fugiat impedit nisi tempora veritatis. Adipisci ea iste necessitatibus
              placeat velit? Maiores molestiae necessitatibus nobis repellendus sit.</p>
            <a class="projects__item-link" href="#">Go to website</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
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
    margin-bottom: 1rem;
    margin-top: 2rem;
    font-size: 2.25rem;
    font-family: 'Oswald';
    font-weight: 100;
    color: white;
    text-align: center;
    letter-spacing: 5px;
    transition: all .3s cubic-bezier(.3, 0, 0, 1.3);
  }

  &-about {
    text-align: center;
    padding: 0 10px;
    position: relative;
    top: -230px;
    font-size: 1rem;
    font-family: 'Oswald';
    font-weight: 100;
    color: white;
    letter-spacing: 5px;
    transition: all .3s cubic-bezier(.3, 0, 0, 1.3);
  }

  &-link {
    position: relative;
    display: block;
    width: 60%;
    top: 200px;
    padding: 10px;
    margin: 10px auto;
    font-family: 'Oswald';
    color: white;
    letter-spacing: 3px;
    text-decoration: none;
    text-align: center;
    border: 2px solid white;
    border-radius: 3px;
    font-size: 1.25em;
    transition: all .3s cubic-bezier(.3, 0, 0, 1.3);

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
      opacity: .75;
    }
  }
}

</style>