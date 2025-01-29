<script>
    export default {
        
    }
</script>

<template>
   <header class="header">
        <a href="#" class="header__head volkhov-regular">FASCO</a>
        <div class="header__link-and-btn">
            <a class="poppins-regular" href="#">Home</a>
            <a class="poppins-regular" href="#">Deals</a>
            <a class="poppins-regular" href="#">New Arrivals</a>
            <a class="poppins-regular" href="#">Packages</a>
            <a class="poppins-regular" href="#">About</a>
            <button class="btn poppins-regular">Sign in</button>
        </div>
  </header>
</template>

<style lang="sass">
.header 
    display: flex
    justify-content: space-between
    max-width: 1280px
    margin: 70px auto 94px

.header__head 
    color: #484848
    font-size: 52px

.header__link-and-btn 
    width: 764px
    justify-content: space-between
    display: flex
    flex-wrap: wrap
    align-items: center
    align-content: center

a 
    text-decoration: none
    color: #484848
    cursor: pointer
    font-size: 16px

.btn 
    padding: 20px 46px
    border-radius: 10px
    color: #FFFFFF
    background-color: #000000
    font-size: 16px
    cursor: pointer

</style>



