<template>
  <div id="app">
    <NavBar></NavBar>
    <Welcome></Welcome>
    <ArticleList></ArticleList>
  </div>
</template>

<script>
  import NavBar from "./components/header/NavBar.vue";
  import Welcome from "./components/header/Welcome.vue";
  import ArticleList from "./components/article/ArticleList.vue";
  export default {
    name: 'App',
    components:{
      'NavBar':NavBar,
      'Welcome':Welcome,
      'ArticleList':ArticleList
    }
  }
</script>

<style>
#app {
  height: 100%;
}
</style>
