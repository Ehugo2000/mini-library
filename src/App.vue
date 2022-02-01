<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> 
      <router-link to="/about">About</router-link>
      <router-link to="/book">Book</router-link>
    </div>

    <router-view :books="books"/>
  </div>
</template>

<script>
import Books from './assets/books.json';

export default {
  data() {
    return {
      books: Books,
    };
  },
  mounted() {
    // console.log(this.books);
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
