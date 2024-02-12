<script>
export default {
    data() {
        return {

        }
    },

    props: {
        image: String,
        brand: String,
        name: String,
        price: String,
    },

    methods:{
    imageCard(imageName){
      return new URL ('../assets/images/' + imageName, import.meta.url).href;
    }
  }
}
</script>

<template>
    <div>
        <img :src="imageCard(image)" alt="">
        <span>{{ brand }}</span>
        <span>{{ name }}</span>
        <span>{{ price }}</span>
    </div>
</template>

<style lang="scss" scoped>
div{
    background-color: aqua;
    width: calc(100% / 3 - 10px);
    display: flex;
    flex-direction: column;
}
</style>