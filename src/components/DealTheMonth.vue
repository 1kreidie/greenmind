<script>
import moment from 'moment';
import Button from './Button.vue';
import Swiper from './Swiper.vue';

export default {
    components: { Button, Swiper },
    data() {
        return {
            unitsOfMeasurements: [
                {
                    value: 'days',
                    period: 'Days'
                },
                {
                    value: 'hours',
                    period: 'Hr'
                },
                {
                    value: 'minutes',
                    period: 'Mins'
                },
                {
                    value: 'seconds',
                    period: 'Sec'
                }
            ],
            timer: null,
            duration: null,
        }
    },
    mounted() {
        const end = moment('2025-08-01')

        this.timer = setInterval(() => {
            if (this.duration !== null && this.duration <= 0) {
                clearInterval(this.timer)
            }

            this.duration = moment.duration(end.diff(moment()))
        }, 1000)
    },
    beforeUnmount() {
        clearInterval(this.timer)
    },
    computed: {
        getDate() {
            return (key) => this.duration?.[key]()
        },
        getUnits() {
            return this.unitsOfMeasurements.filter((el) => !!this.getDate(el.value) || el.value === 'seconds')
        }
    },
}
</script>

<template>
    <section class="deals-of-month">
        <div class="box-mounth" style="overflow: hidden">
            <div class="box__info">
                <div class="deals-of-month__info">
                    <h1 class="title volkhov-regular">Deals Of The Month</h1>
                    <p class="text poppins-regular">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis ultrices sollicitudin aliquam sem. Scelerisque duis ultrices sollicitudin </p>
                    <Button>Buy Now</Button>
                </div>
                <template v-if="getUnits.length > 1">
                    <h2 class="timer__title poppins-medium">Hurry, Before It’s Too Late!</h2>
                    <div class="timer">
                        <div class="timer__span" v-for="(item, id) in getUnits" :key="id" >
                            <div class="style-time time">{{ getDate(item.value) }}</div>
                            <p class="style-p unitsOfMeasurement">{{ item.period }}</p>
                        </div>
                    </div>
                </template>
            </div>
            <div class="box__swiper">
                <Swiper />
            </div>
        </div>
    </section>
    
</template>

<style lang="sass" scoped>
.deals-of-month
    box-shadow: inset 0px 7px 15px -3px rgba(0,0,0,0.1),inset 0px -7px 15px -3px rgba(0,0,0,0.1)
    &__info
        padding-top: 155px
        padding-bottom: 50px
        width: 444px

.box-mounth
    margin-left: 400px
    display: flex

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
    min-width: 56px

.style-p
    margin-top: 25px

.box__swiper
    width: 1196px
    margin: 155px 0
    margin-left: 122px
</style>