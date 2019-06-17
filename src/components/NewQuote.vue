<template>
  <div class="container new-quote">
    <p>Quote</p>
    <textarea type="text" class="form-control" v-model="quote" />
    <button class="btn btn-primary" @click="addQuote(quote)">Add Quote</button>
  </div>
</template>
<script>
export default {
  props: {
    pushQuote: {
      type: Function
    },
    canAdd: {
      type: Boolean
    }
  },
  data: function() {
    return {
      quote: ""
    };
  },
  methods: {
    addQuote(quote) {
      this.$props.canAdd && this.quote && this.$props.pushQuote(quote);
      this.quote = "";
    }
  }
};
</script>

<style>
.new-quote {
  text-align: center;
}
.btn {
  margin: 1rem 0;
}

.form-control {
  max-width: 40rem;
  margin: 0 auto;
}
</style>
