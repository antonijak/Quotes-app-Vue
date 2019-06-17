<template>
  <div class="container all-quotes">
    <single-quote
      v-for="quote in quotes"
      :quote="quote"
      :deleteQuote="deleteQuote"
    >
    </single-quote>
  </div>
</template>
<script>
import SingleQuote from "./SingleQuote.vue";
export default {
  props: {
    quotes: {
      type: Array
    },
    deleteQuote: {
      type: Function
    }
  },
  components: {
    singleQuote: SingleQuote
  }
};
</script>

<style>
.all-quotes {
  display: flex;
  flex-wrap: wrap;
}
</style>
