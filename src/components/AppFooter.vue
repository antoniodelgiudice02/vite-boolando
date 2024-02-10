
<script>

export default {
  data() {
    return {
      links: [
        { link: 'Informazioni legali' },
        { link: 'Informativa sulla privacy' },
        { link: 'Diritto di recesso' }
      ],

      socials: [
        { social: 'fa-brands fa-square-twitter' },
        { social: 'fa-brands fa-square-facebook' },
        { social: 'fa-brands fa-square-twitter' },
        { social: 'fa-brands fa-square-facebook' },
        { social: 'fa-brands fa-square-facebook' },
        

        
      ],

    }
  }
}

</script>

<template>
  <footer>

    <div>
      <div>
        <div>
          <span>Boolando s.r.l.</span>
        </div>
        <ul>
          <li v-for="link in links"><a href="">{{ link.link }}</a></li>
        </ul>
      </div>
    </div>

    <div>
      <div>
        <div>
          <span>Trovaci anche su</span>
        </div>
        <ul>
          <li v-for="social in socials"><a href=""><i :class="social.social"></i></a></li>
        </ul>
      </div>
    </div>

  </footer>
</template>

<style lang="scss" scoped>
footer {
  height: 60px;
  background-color: #1a1a1a;
  color: white;

  

  li {
    font-size: 0.6rem;
    display: inline;
    margin: 0 5px;
  }

  span {
    margin: 0 5px;
  }

  i{
    font-size: 1rem;
  }
}
</style>