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
    <div class="card">
        <img :src="image" alt="image">
        <h3>{{ title }}</h3>
        <p>{{ manufacturer }}</p>
        <p>{{ income }}</p>
        <span>${{ price }}</span>
        <p>{{ state }}</p>
    </div>
</template>

<style lang="sass" scoped>
.card
    
</style>