<script>
import Header from './components/Header.vue';
export default{
  components: { Header },
  data(){
    return{

    }
  }
}
</script>

<template>
  <div>
    <Header></Header>
    <div class="wrapper">
      <div class="man-wrapper">
        <img class="man-wrapper__man-img" src="../src/assets/img/img1.svg" alt="man">
      </div>
      <div class="center-column">
        <div class="girls-top">
          <img class="girls-top__img" src="../src/assets/img/img2.svg" alt="girl">
        </div>
        <div class="block-center">
          <h1 class="block-center__first poppins-medium">ULTIMATE</h1>
          <h1 class="block-center__second poppins-medium">SALE</h1>
          <p class="block-center__paragraph poppins-regular">NEW COLLECTION</p>
          <button class="block-center__btn poppins-medium">SHOP NOW</button>
        </div>
        <img src="../src/assets/img/img3.png" alt="girl">
      </div>
      <div class="man-wrapper man-right">
        <img class="man-wrapper__man-img" src="../src/assets/img/img4.svg" alt="man">
      </div>
      
    </div>
    <div class="icon">
        <button class="icon__basket">
          <img src="../src/assets/img/icon.svg" alt="icon">
        </button>
        <button class="icon__up">
          <img src="../src/assets/img/vector.svg" alt="icon">
        </button>
      </div>
  </div>
</template>



<style lang="sass">
$color: #484848
$color-btn: #000
$pointer: pointer


.wrapper 
  max-width: 1280px
  margin: 0 auto
  position: relative
  height: 756px

.man-wrapper 
  width: 392px
  height: 756px
  background-color: #E0E0E0
  position: absolute
  border-radius: 20px

  &__man-img
    position: absolute
    bottom: 0

.man-right 
  right: 0
  top: 0

.center-column
  position: absolute
  display: flex
  flex-direction: column
  right: 440px
  height: 756px

.girls-top 
  width: 426px
  height: 150px
  background-color: #E0E0E0
  border-radius: 20px

  &__img 
    position: absolute
    top: 5px
    left: 13px

.block-center 
  display: flex
  flex-direction: column 
  flex-wrap: nowrap
  position: relative
  align-items: center
  padding-bottom: 36px

  &__first
    font-size: 91px
    color: $color
    margin: 0
    line-height: 100%

  &__second
    font-size: 187px
    color: #fff
    line-height: 100%
    -webkit-text-stroke: 1px $color
    
  &__paragraph
    font-size: 20px
    color: $color
    padding: 25px 0 19px 0

  &__btn
    padding: 20px 60px
    border-radius: 10px
    color: #FFFFFF
    background-color: $color-btn
    font-size: 16px
    cursor: $pointer

.icon
  display: flex
  gap: 35px
  position: fixed
  right: 40px
  bottom: 30px

  &__basket
    padding: 18px 18px 18px 16px
    background-color: $color-btn
    border-radius: 10px
    cursor: $pointer

  &__up
    padding: 15px 20px
    border-radius: 100%
    border: 2px solid $color-btn
    cursor: $pointer
</style>