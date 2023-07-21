<template>
  <div class="Index">
    <KeyVision />
    <div class="result"></div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
<style lang="scss">
.Index {
  overflow-x: hidden; 
  background-image: url('~/assets/background.jpg');
  background-size: cover;
  background-position: center;
  .result {
    padding-top: 100px;
  }
}
</style>
