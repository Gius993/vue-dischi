<template>
  <div id="app">

      <PageHeader />
      <MainPage />
  </div>
</template>

<script>

  import PageHeader from './components/PageHeader.vue'
  import MainPage from './components/MainPage.vue'
  export default {
    name: 'App',
     components: {
    
       PageHeader,
       MainPage
  },

}
</script>

<style lang="scss">
    @import './style/common.scss';
     @import  './style/variables.scss';
</style>
