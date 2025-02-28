<script>
import Button from './Button.vue';
    export default {
        components:{ Button}
    }
</script>

<template>
    <section class="peaky-blinders">
        <div class="box-peaky">
            <div class="peaky-blinders__image">
                <img src="../assets/img/peaky-blinders.png" alt="img">
            </div>
            <div class="peaky-blinders__content">
                <p class="text-default poppins-regular">Women Collection</p>
                <h1 style="color: #484848; font-size: 46px;" class="volkhov-regular">Peaky Blinders</h1>
                <p style="text-decoration: underline; font-size: 16px" class="poppins-regular">DESCRIPTION</p>
                <p class="text-default poppins-regular">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis ultrices sollicitudin aliquam sem. Scelerisque duis ultrices sollicitudin. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis.</p>
                <div class="size">
                    <p class="size__title poppins-regular">Size</p>
                    <button class="size__btn">m</button>
                </div>
                <span style="font-size: 28px;" class="poppins-medium">$100.00</span>
                <Button>Buy Now</Button>
            </div>
        </div>
    </section>
</template>



<style lang="sass" scoped>
.text-default
    color: #767676
    font-size: 16px

.box-peaky
    margin-left: 400px
    display: flex
    right: 300px

.peaky-blinders
    display: flex
    align-items: center
    justify-content: center
    background-color: #DADADA
    &__content
        gap: 20px
        display: flex
        flex-direction: column
        height: 570px
        padding: 60px 321px 60px 282px
    &__image
        position: absolute
        left: 0
.size
    display: flex
    align-items: center
    gap: 15px
    &__btn
        padding: 6px 20px
        border-radius: 10px
        color: #FFFFFF
        background-color: #000000
        font-size: 16px
        cursor: pointer
    &__title
        color: #767676
</style>