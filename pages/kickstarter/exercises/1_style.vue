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
  color: purple;
}

.promo {
  color: red;
}

#uni-p {
  color: orange;
}
</style>
