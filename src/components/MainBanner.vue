<template>
  <div class="stars-wrapper">
    <div class="stars stars-1"></div>
    <div class="stars stars-2"></div>
    <div class="stars stars-3"></div>
  </div>
  <div class="app-container main">
    <div class="image">
      <img src="https://picsum.photos/200/300" alt="">
    </div>
    <div class="text-content">
      <p>Hi, There!</p>
      <h2>
        I'm A Marina Dubyna!
      </h2>
      <h1>
        I'm A Frontend Developer!
      </h1>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="sass" scoped>
.main
  z-index: 2
  width: 500px
  height: 500px
  position: absolute
  top: 50%
  left: 50%
  transform: translate(-50%, -50%)
  display: flex
  flex-direction: column
  align-items: center

.image
  width: 400px
  height: 400px
  border-radius: 20%

  & img
    width: 100%
    height: 100%
    object-fit: cover
    border-radius: 20%

.text-content
  color: white
  text-align: center
  width: 100%
  max-width: 300px


@function random-value()
  @return random(2000)

@mixin multiple-box-shadow($n)
  $shadow-values: ()
  @for $i from 1 through $n
    $x: random-value() + px
    $y: random-value() + px
    $color: #FFF
    $shadow-values: append($shadow-values, $x $y $color, comma)
  box-shadow: $shadow-values


.stars
  position: absolute
  left: 0
  max-height: 100vh
  z-index: 1

  &-wrapper
    position: relative
    height: 100vh
    max-height: 100vh
    background: linear-gradient(to bottom, #505050, #080808) no-repeat #080808

.stars-1
  width: 1px
  height: 1px
  background: transparent
  @include multiple-box-shadow(100)
  animation: animStar 50s linear infinite

  &:after
    content: " "
    position: absolute
    //top: 2000px
    width: 1px
    height: 1px
    background: transparent
    @include multiple-box-shadow(100)

.stars-2
  width: 2px
  height: 2px
  background: transparent
  @include multiple-box-shadow(200)
  animation: animStar 100s linear infinite

  &:after
    content: " "
    position: absolute
    //top: 2000px
    width: 2px
    height: 2px
    background: transparent
    @include multiple-box-shadow(200)

.stars-3
  width: 3px
  height: 3px
  background: transparent
  @include multiple-box-shadow(300)
  animation: animStar 150s linear infinite

  &:after
    content: " "
    position: absolute
    //top: 2000px
    width: 3px
    height: 3px
    background: transparent
    @include multiple-box-shadow(300)

@keyframes animStar
  from
    transform: translateY(0px)
  to
    transform: translateY(-2000px)
</style>