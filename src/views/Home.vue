<template>
  <div id="home">
    <h3>List of books</h3>
    <ul>
      <li v-for="book in books" :key="book.id">
        <span>
          {{ book.Title }}
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['books'],
  mounted() {
    console.log(this.books);
  },
};
</script>

<style scoped>
li {
  list-style: none;
}
</style>
