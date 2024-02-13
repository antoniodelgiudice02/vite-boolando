<script>
export default {
    data() {
        return {

        }
    },

    props: {
        frontImage: String,
        backImage: String,
        brand: String,
        name: String,
        price: String,
        sale: String,
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

        <img :src="imageCard(frontImage)" alt="">
        <!-- <img :src="imageCard(backImage)" alt=""> -->
        <span>{{ brand }}</span>
        <span>{{ name }}</span>
        <span class="price">{{ price }} €</span>

        <div class="badges">
            <span class="sale">{{ sale }}</span>
        </div>

    </div>
</template>

<style lang="scss" scoped>
div{
    width: calc(100% / 3 - 10px);
    display: flex;
    flex-direction: column;
    position: relative;

    .price{
        color: red;
    }

    .badges{
        position: absolute;
        background-color: green;
    }
}
</style>