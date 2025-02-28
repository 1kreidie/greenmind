<script>
    export default {
        props: ({
            image: {
                type: String,
                default: null
            },
            title: {
                type: String,
                default: null
            },
            manufacturer: {
                type: String,
                default: null
            },
            income: {
                type: String,
                default: null
            },
            price: {
                type: Number,
                default: null
            },
            state: {
                type: String,
                default: null
            }
        })
    }
</script>

<template>
    <div class="card poppins-medium">
        <img :src="image" alt="image">
        <div class="card__info">
            <div>
                <h3 style="font-size: 20px;">{{ title }}</h3>
                <p style="color: #8A8A8A; font-size: 12px;">{{ manufacturer }}</p>
                <p style="font-size: 12px; padding: 25px 0;">{{ income }}</p>
                <span style="font-size: 24px;">${{ price }}</span>
            </div>
            <div class="info-right">
                <p class="poppins-regular" style="color: #FF4646; font-size: 12px;">{{ state }}</p>
                <svg width="0" height="0" xmlns="http://www.w3.org/2000/svg">
                    <symbol xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32" id="star">
                    <path d="M31.547 12a.848.848 0 00-.677-.577l-9.427-1.376-4.224-8.532a.847.847 0 00-1.516 0l-4.218 8.534-9.427 1.355a.847.847 0 00-.467 1.467l6.823 6.664-1.612 9.375a.847.847 0 001.23.893l8.428-4.434 8.432 4.432a.847.847 0 001.229-.894l-1.615-9.373 6.822-6.665a.845.845 0 00.214-.869z" />
                    </symbol>
                </svg>
                <p class="c-rate">
                    <svg class="c-icon active" width="32" height="32">
                        <use xlink:href="#star"></use>
                    </svg>
                    <svg class="c-icon active" width="32" height="32">
                        <use xlink:href="#star"></use>
                    </svg>
                    <svg class="c-icon active" width="32" height="32">
                        <use xlink:href="#star"></use>
                    </svg>
                    <svg class="c-icon active" width="32" height="32">
                        <use xlink:href="#star"></use>
                    </svg>
                    <svg class="c-icon" width="32" height="32">
                        <use xlink:href="#star"></use>
                    </svg>
                </p>
            </div>
        </div>
    </div>
</template>

<style lang="sass" scoped>
.card
    padding: 15px 25px 36px
    border-radius: 20px
    background-color: #FFFFFF
    box-shadow: 0px 1px 10px -3px rgba(0, 0, 0, 0.1)
    &__info
        display: flex
        justify-content: space-between
        padding-top: 12px 
.info-right
    display: flex
    flex-direction: column-reverse
    flex-wrap: wrap
    align-items: flex-end
    align-content: center
    justify-content: space-between

.c-icon 
    --star-active: #fece3c
    --star-inactive: #6c6962
    fill: var(--star-inactive)

.c-icon.active 
    fill: var(--star-active)

</style>