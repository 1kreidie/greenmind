<script>
import BrandLogos from './components/BrandLogos.vue';
import DealTheMonth from './components/DealTheMonth.vue';
import Header from './components/Header.vue';
import UltimateSale from './components/UltimateSale.vue';
import NewArrivals from './components/NewArrivals.vue';

export default {
  components: {
    Header,
    UltimateSale,
    DealTheMonth,
    BrandLogos,
    NewArrivals
  },
  data() {
    return {
      items: [
        {
          image: '../src/assets/img/logo1.svg'
        },
        {
          image: '../src/assets/img/logo2.svg'
        },
        {
          image: '../src/assets/img/logo3.svg'
        },
        {
          image: '../src/assets/img/logo4.svg'
        },
        {
          image: '../src/assets/img/logo5.svg'
        }
      ],
      
    }
  }
}
</script>

<template>
  <div class="box">
    <Header/>
    <UltimateSale/>
    <div class="brands-box">
    <BrandLogos 
      v-for="item in items"
      :key="item"
      :image="item.image"/>
    </div>
    <div class="deal-box">
      <DealTheMonth/>
    </div>
    <NewArrivals/>
  </div>
</template>



<style lang="sass">
$color: #484848
$color-btn: #000
$pointer: pointer


.box
  max-width: 1280px
  margin: 0 auto
  
.brands-box
  display: flex
  justify-content: space-between
  padding: 82px 0

.deal-box
  width: 100%
  justify-content: center
  display: flex

.wrapper 
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
  z-index: 100

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