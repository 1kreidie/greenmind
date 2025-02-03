<script>
import Button from './Button.vue';
export default{
    name: 'DealTheMonth',
    components: { Button }
}
</script>
<template>
    <section class="wrapper">
        <div class="man-wrapper">
            <img class="man-wrapper__man-img" src="../assets/img/img1.svg" alt="man">
        </div>
        <div class="center-column">
            <div class="girls-top">
                <img class="girls-top__img" src="../assets/img/img2.svg" alt="girl">
            </div>
            <div class="block-center">
                <h1 class="block-center__first poppins-medium">ULTIMATE</h1>
                <h1 class="block-center__second poppins-medium">SALE</h1>
                <p class="block-center__paragraph poppins-regular">NEW COLLECTION</p>
                <Button style="padding: 20px 60px;">SHOP NOW</Button>
            </div>
            <img src="../assets/img/img3.png" alt="girl">
        </div>
        <div class="man-wrapper man-right">
            <img class="man-wrapper__man-img" src="../assets/img/img4.svg" alt="man">
        </div>
        <div class="icon">
            <button class="icon__basket">
                <img src="../assets/img/icon.svg" alt="icon">
            </button>
            <button class="icon__up">
                <img src="../assets/img/vector.svg" alt="icon">
            </button>
        </div>
    </section>
</template>
<style lang="sass">

</style>