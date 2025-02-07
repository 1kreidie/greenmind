<script>
    export default {
        props: ({
            image: {
                type: String,
                default: null
            }
        })
    }
</script>

<template>
    <img :src="image" alt="brand-logo">
</template>
