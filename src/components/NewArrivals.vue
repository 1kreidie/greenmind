<script>
import Button from './Button.vue';
import Card from './Card.vue';
    export default {
        components: { Button, Card },
        data() {
            return {
                items:[
                    { content: 'Men’s Fashion' },
                    { content: 'Women’s Fashion' },
                    { content: 'Women Accessories' },
                    { content: 'Men Accessories' },
                    { content: 'Discount Deals' },
                ],
                carts: [
                    {
                        image: '../src/assets/img/img-cart1.png',
                        title: 'Shiny Dress',
                        manufacturer: 'Al Karam',
                        income: '(4.1k) Customer Reviews',
                        price: 95.50,
                        state: 'Almost Sold Out'
                    },
                    {
                        image: '../src/assets/img/img-cart2.png',
                        title: 'Shiny Dress',
                        manufacturer: 'Al Karam',
                        income: '(4.1k) Customer Reviews',
                        price: 95.50,
                        state: 'Almost Sold Out'
                    },
                    {
                        image: '../src/assets/img/img-cart3.png',
                        title: 'Shiny Dress',
                        manufacturer: 'Al Karam',
                        income: '(4.1k) Customer Reviews',
                        price: 95.50,
                        state: 'Almost Sold Out'
                    },
                    {
                        image: '../src/assets/img/img-cart4.png',
                        title: 'Shiny Dress',
                        manufacturer: 'Al Karam',
                        income: '(4.1k) Customer Reviews',
                        price: 95.50,
                        state: 'Almost Sold Out'
                    },
                    {
                        image: '../src/assets/img/img-cart5.png',
                        title: 'Shiny Dress',
                        manufacturer: 'Al Karam',
                        income: '(4.1k) Customer Reviews',
                        price: 95.50,
                        state: 'Almost Sold Out'
                    },
                    {
                        image: '../src/assets/img/img-cart6.png',
                        title: 'Shiny Dress',
                        manufacturer: 'Al Karam',
                        income: '(4.1k) Customer Reviews',
                        price: 95.50,
                        state: 'Almost Sold Out'
                    },
                ]
            }
        },
        
    }
</script>

<template>
    <section class="new-arrivals">
        <div class="new-arrivals__title">
            <h1 class="header">New Arrivals</h1>
            <p class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis ultrices sollicitudin aliquam sem. Scelerisque duis ultrices sollicitudin </p>
        </div>
        <div class="new-arrivals__buttons">
            <button class="button" v-for="item in items" :key="item">{{ item.content }}</button>
        </div>
        <div class="new-arrivals__wrapper">
            <Card
                v-for="cart in carts"
                :key="cart"
                :image="cart.image"
                :title="cart.title"
                :manufacturer="cart.manufacturer"
                :income="cart.income"
                :price="cart.price"
                :state="cart.state"/>
        </div>
        <Button>View More</Button>
    </section>
</template>


<style lang="sass" scoped>

.new-arrivals
    margin: 150px 0 150px 0
    &__title
        display: flex
        flex-direction: column
        flex-wrap: nowrap
        align-items: center

    &__buttons
        display: flex
        flex-direction: row
        flex-wrap: wrap
        justify-content: center
        gap: 30px
    &__wrapper
        display: flex
        flex-wrap: wrap
        gap: 60px
        width: 1280px
        padding: 50px 0
        justify-content: center
.header
    font-size: 48px
    text-align: center
.text
    width: 614px
    padding: 20px 0 50px 0
    font-size: 16px
    color: #8A8A8A
    text-align: center

.button
    width: 207px
    height: 56px
    border-radius: 10px
    color: #8A8A8A
    background-color: #FAFAFA
    font-size: 16px
    cursor: pointer

.button:focus
    color: #FFFFFF
    background-color: #000000
</style>