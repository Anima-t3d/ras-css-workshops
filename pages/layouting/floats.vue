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
      <div class="blue top left"></div>
      <div class="blue top right"></div>
      <div class="blue bottom left"></div>
      <div class="blue bottom right"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Floats',
  layout: 'layouting',
}
</script>

<style lang="scss" scoped>
.flags {
  .flag {
    float: left;

    margin-left: calc((100vw - 3 * 320px) / 2);

    &:first-child {
      margin-left: 0;
    }

    &:hover {
      cursor: help;

      &::after {
        content: attr(data-country);
      }
    }
  }
}

.flag {
  width: 320px;
  height: 180px;

  .top,
  .bottom {
    width: 150px;
    height: 80px;
  }

  .bottom {
    margin-top: 20px;
  }

  .left {
    width: 100px;
  }

  .right {
    width: 200px;
  }
}
.stripes-3 {
  > div {
    width: 100%;
    height: 33.33%;
  }
  &.vertical {
    > div {
      float: left;

      width: 33.33%;
      height: 100%;
    }
  }
}

.left {
  float: left;
}
.right {
  float: right;
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
