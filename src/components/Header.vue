<template>
  <header>
    <h1>Quotes added</h1>
    <div class="progress">
      <div
        class="progress-bar"
        role="progressbar"
        :style="{ width: width.toString() * 11.111111 + '%' }"
      >
        {{ width }}/9
      </div>
    </div>
  </header>
</template>
<script>
export default {
  props: {
    width: {
      type: Number
    }
  }
};
</script>

<style></style>
