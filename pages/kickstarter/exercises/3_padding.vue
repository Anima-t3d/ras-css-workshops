<template>
  <div class="example">
    <p>This is p1</p>
    <p class="promo">This is p2</p>
    <p>This is p3</p>
    <p id="uni-p">This is unique!</p>
    <p>This is p5</p>
    <p class="promo">This is p6</p>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.example {
  background: white;
}

p {
  padding: 16px;

  color: white;
  background: purple;
}

.promo {
  padding-left: 32px;

  background: red;
}

#uni-p {
  padding: 0;

  background: orange;
}
</style>
