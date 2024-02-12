<script>

export default {
  data() {
    return {
      reparto: [
        {name: 'Donna'},
        {name: 'Uomo'},
        {name: 'Bambino'}
      ],

      logo: '../assets/images/boolean-logo.png',

      userArea: [
        {area: 'fa-regular fa-user'},
        {area: 'fa-regular fa-heart'},
        {area: 'fa-solid fa-bag-shopping'},
      ]
    }
  },

  methods:{
    image(imageName){
      return new URL (imageName, import.meta.url).href;
    }
  }
}

</script>

<template>

  <header>
    <div>
      <ul>
        <li v-for="genere in reparto">{{ genere.name }}</li>
      </ul>
    </div>
    <div>
      <img :src="image(logo)" alt="">
    </div>
    <div>
      <ul>
        <li v-for="areas in userArea"><i :class="areas.area"></i></li>
      </ul>
    </div>
  </header>

</template>

<style lang="scss" scoped>

  header{
    height: 60px;
    background-color: #ff6900;
    color: white;
    

    li{
      display: inline;
      margin: 0 10px;
    }

    img{
      height: 30px;
    }
  }

</style>
