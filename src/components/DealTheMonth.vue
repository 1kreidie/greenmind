<script>
import Button from './Button.vue';
import Swiper from './Swiper.vue';
export default {
    components:{ Button, Swiper },
    data() {
        return {
            interval: 1000,
            unitsOfMeasurements: [{
                id: 1,
                value: 20,
                period: 'Days'
            },
            {
                id: 2,
                value: 6,
                period: 'Hr'
            },
            {
                id: 3,
                value: 55,
                period: 'Mins'
            },
            {
                id: 4,
                value: 30,
                period: 'Sec'
            }]
        }
    },
    methods: {

    }

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
            <h2 class="timer__title poppins-medium">Hurry, Before It’s Too Late!</h2>
            <div class="timer">
                <div class="timer__span" v-for="(item, id) in unitsOfMeasurements" :key="id" >
                    <span class="style-time  time">{{ item.value }}</span>
                    <p class="style-p unitsOfMeasurement">{{ item.period }}</p>
                </div>
            </div>
            <Swiper style="margin: 200px 0"/>
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
    display: flex
    margin-top: 15px
    justify-content: space-between
    &__title
        font-size: 28px
        color: #484848
    &__span
        text-align: center
    
.style-time
    padding: 16px 12px
    box-shadow: inset 0px 7px 15px -3px rgba(0,0,0,0.1),inset 0px -7px 15px -3px rgba(0,0,0,0.1)
    border-radius: 10px
    font-size: 32px

.style-p
    margin-top: 25px

</style>