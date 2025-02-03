<script>
import Button from './Button.vue';
export default {
    components:{ Button }
}
</script>

<template>
    <section class="deals-of-month">
      <div class="deals-of-month__info">
            <h1 class="title volkhov-regular">Deals Of The Month</h1>
            <p class="text poppins-regular">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis ultrices sollicitudin aliquam sem. Scelerisque duis ultrices sollicitudin </p>
            <Button>Buy Now</Button>
      </div>
        <div class="timer">
            <h2 class="timer__title">Hurry, Before It’s Too Late!</h2>
            <div class="timer__span">
                <span class="style-span">02</span>
                <p class="style-p">Days</p>
            </div><div class="timer__span">
                <span class="style-span">02</span>
                <p class="style-p">Days</p>
            </div>
            
        </div>
      <div class="deals-of-month__slider">
      </div>
    </section>
</template>

<style lang="sass" scoped>
.deals-of-month 
    box-shadow: inset 0px 7px 15px -3px rgba(0,0,0,0.1),inset 0px -7px 15px -3px rgba(0,0,0,0.1)

.deals-of-month__info
    padding-top: 155px
    width: 444px

.title
    font-size: 46px
    line-height: 100%

.text
    font-size: 16px
    padding: 20px 0 40px 0

.timer__span
    display: flex
    flex-direction: column
    align-items: center
    width: 394px
</style>