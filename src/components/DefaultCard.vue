<template>
  <div>
    <div class="Card"></div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.Card {
  width: 200px;
  height: 232px;
  border-radius: 5px;
  border: 1px solid #666;
  transition: box-shadow 0.5s;
  margin-left: 15px;
  background-image: url("../assets/vue-js.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  box-shadow: 0px 9px 55px #666;
}

.Card img {
  width: 100%;
  height: 100%;
}
</style>