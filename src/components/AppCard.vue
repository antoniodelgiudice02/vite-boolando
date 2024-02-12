<script>
export default {
    data() {
        return {

        }
    },

    props: {
        brand: String,
    }
}
</script>

<template>
    <div><span>{{ brand }}</span></div>
</template>

<style lang="scss" scoped>
div{
    background-color: aqua;
    width: calc(100% / 3 - 10px);
}
</style>