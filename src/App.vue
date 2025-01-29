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
        <img class="man-left" src="../src/assets/img/img1.svg" alt="man">
      </div>
      <div class="center-column">
        <div class="girls-top">
          <img class="girl-top" src="../src/assets/img/img2.svg" alt="girl">
        </div>
        <div class="block-center">
          <h1 class="block-center__first poppins-medium">ULTIMATE</h1>
          <h1 class="block-center__second poppins-medium">SALE</h1>
          <p class="block-center__paragraph">NEW COLLECTION</p>
          <button class="block-center__btn">SHOP NOW</button>
        </div>
        <div class="girls-bottom">
          <img src="../src/assets/img/img3.png" alt="girl">
        </div>
      </div>
      <div class="man-wrapper man-wrapper__right">
        <img class="man-right" src="../src/assets/img/img4.svg" alt="man">
      </div>
    </div>
  </div>
</template>



<style lang="sass">
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

.man-wrapper__right 
  right: 0
  top: 0

.man-left 
  position: absolute
  bottom: 0

.man-right 
  position: absolute
  bottom: 0

.girls-top 
  width: 426px
  height: 150px
  background-color: #E0E0E0
  border-radius: 20px
  /* position: absolute */
  /* left: 432px */

.girl-top 
  position: absolute
  top: 0

/* .block-center 
  display: flex
  flex-direction: column
  flex-wrap: nowrap
  align-items: center
  position: relative
  top: 90px
  width: 400px
  height: 384px
 */
.block-center__first
  font-size: 91px

.block-center__second
  font-size: 187px
  padding-top: -20px
  
.center-column
  display: flex
  flex-direction: row
  flex-wrap: wrap
  position: absolute
  right: 440px
  height: 756px

</style>