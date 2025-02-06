<script>
import Button from './Button.vue';
export default {
    components:{ Button }
}
</script>

<template>
    <section style="position: absolute; left: 0; right: 0; box-shadow: inset 0px 7px 15px -3px rgba(0,0,0,0.1),inset 0px -7px 15px -3px rgba(0,0,0,0.1)" class="deals-of-month">
        <div class="box">
            <div class="deals-of-month__info">
                <h1 class="title volkhov-regular">Deals Of The Month</h1>
                <p class="text poppins-regular">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis ultrices sollicitudin aliquam sem. Scelerisque duis ultrices sollicitudin </p>
                <Button>Buy Now</Button>
            </div>
            <div class="timer">
                <h2 class="timer__title poppins-medium">Hurry, Before It’s Too Late!</h2>
                <div class="timer__span">
                    <span class="style-span">{{  }}</span>
                    <p class="style-p">{{  }}</p>
                </div>
            </div>
            <div class="deals-of-month__slider">
            </div>
        </div>
      
    </section>
</template>

<style lang="sass" >

.deals-of-month__info
    padding-top: 155px
    padding-bottom: 50px
    width: 444px

.title
    font-size: 46px
    line-height: 100%
    

.text
    font-size: 16px
    padding: 20px 0 40px 0
    color: #8A8A8A
.timer
    width: 394px
    &__title
        font-size: 28px
        color: #484848
    &__span
        display: flex
        flex-direction: column
        align-items: center
        width: 394px
</style>