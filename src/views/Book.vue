<template>
  <div id="book">
    <h3>Book</h3>
    <p>{{book.Title}}</p>
    <p>{{book.Author}}</p>
    <p>{{book.Audience}}</p>
  </div>
</template>

<script>
export default {
  props: ['books'],
  mounted() {
    console.log(this.$route.params.id);
    let book = this.books.find(book => book.Id == this.$route.params.id)
    console.log(book);
    this.book = book
  },
  data() {return {
    book: null,
  }}
};
</script>

<style></style>
