<template>
  <div class="container app">
    <app-header :width="quotes.length"></app-header>
    <new-quote
      :quote="newQuote"
      :pushQuote="pushQuote"
      :canAdd="quotes.length < 9"
    ></new-quote>
    <all-quotes :quotes="quotes" :deleteQuote="deleteQuote"></all-quotes>
    <div class="alert alert-info" role="alert">
      Info: Click on a Quote to delete it
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import NewQuote from "./components/NewQuote.vue";
import AllQuotes from "./components/AllQuotes.vue";

export default {
  data: function() {
    return {
      quotes: [],
      newQuote: ""
    };
  },
  methods: {
    pushQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(quote) {
      this.quotes = this.quotes.filter(item => item !== quote);
    }
  },
  components: {
    allQuotes: AllQuotes,
    appHeader: Header,
    newQuote: NewQuote
  }
};
</script>

<style scoped></style>
