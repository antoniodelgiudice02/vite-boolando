<script>
import AppHeader from './components/layout/AppHeader.vue'
import AppMain from './components/layout/AppMain.vue'
import AppFooter from './components/layout/AppFooter.vue'
export default {
  data() {
    return {

    }
  },

  components: {AppHeader, AppMain, AppFooter}
}
</script>

<template>
  <app-header></app-header>
  <app-main></app-main>
  <app-footer></app-footer>

</template>

<style lang="scss">
@use './styles/general.scss' 
</style>
