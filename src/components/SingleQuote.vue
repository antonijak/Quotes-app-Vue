<template>
  <div class="card" @click="deleteQuote(quote)">
    <div class="card-body">
      <p class="card-text">{{ quote }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    quote: {
      type: String
    },
    deleteQuote: {
      type: Function
    }
  }
};
</script>

<style scoped>
.card {
  position: relative;
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -webkit-flex-direction: column;
  -ms-flex-direction: column;
  flex-direction: column;
  background-color: #fff;
  border: 1px solid rgba(0, 0, 0, 0.125);
  border-radius: 0.25rem;
  margin: 1rem;
  width: 30%;
}

.card:hover {
  background: #ffc5c3;
}
.card-text {
  text-align: center;
  padding: 1rem;
  margin: 0;
  font-family: Arizonia;
  font-size: 3rem;
}
</style>
