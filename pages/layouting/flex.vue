<template>
  <div class="flags">
    <div class="flag stripes-3 vertical" data-country="Belgium">
      <div class="black"></div>
      <div class="yellow"></div>
      <div class="red"></div>
    </div>
    <div class="flag stripes-3" data-country="Germany">
      <div class="black"></div>
      <div class="red"></div>
      <div class="yellow"></div>
    </div>
    <div class="flag yellow" data-country="Sweden">
      <div class="row">
        <div class="blue left"></div>
        <div class="blue right"></div>
      </div>
      <div class="row">
        <div class="blue left"></div>
        <div class="blue right"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Flex',
  layout: 'layouting',
}
</script>

<style lang="scss" scoped>
.flags {
  display: flex;
  justify-content: space-between;

  .flag {
    &:hover {
      position: relative;

      cursor: help;

      &::after {
        position: absolute;
        bottom: -20px;
        left: 0;

        content: attr(data-country);
      }
    }
  }
}

.flag {
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  width: 320px;
  height: 180px;

  .row {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    > div {
      width: 150px;
      height: 80px;
    }
  }

  .left {
    flex: 0 0 100px;
  }

  .right {
    flex: 0 0 200px;
  }
}
.stripes-3 {
  display: flex;
  flex-direction: column;

  > div {
    width: 100%;
    height: 33.33%;
  }
  &.vertical {
    flex-direction: row;
    > div {
      width: 33.33%;
      height: 100%;
    }
  }
}

.black {
  background-color: black;
}
.red {
  background-color: red;
}
.yellow {
  background-color: yellow;
}
.blue {
  background-color: blue;
}
</style>
