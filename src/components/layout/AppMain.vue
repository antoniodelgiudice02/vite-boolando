<script>

import AppCard from '../AppCard.vue'
import axios from 'axios';
import { store } from '../store'

export default {
  data() {
    return {

      products: []
      
    }
  },

  created(){
    axios.get( `${store.apiUri}/products`).then((response) => {
      this.products = response.data;
    })
  },

  components: { AppCard },
}

</script>

<template>
  <main>
    <div class="card-container">

      <app-card v-for="product in products" 
        :frontImage="product.frontImage"
        :backImage="product.backImage"
        :brand="product.brand" 
        :name="product.name" 
        :price="product.price">
      </app-card>

    </div>
  </main>
</template>

<style lang="scss" scoped>
.card-container {
  width: 100%;
  display: flex;
  justify-content: space-between;
  gap: 10px;
  flex-wrap: wrap;
  padding: 25px;
  margin: 10px;
}
</style>