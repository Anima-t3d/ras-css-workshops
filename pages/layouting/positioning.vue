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
  name: 'Positioning',
  layout: 'layouting',
}
</script>

<style lang="scss" scoped>
.flags {
  position: relative;

  .flag {
    position: absolute;
    top: 0;
    left: 50%;

    &:first-child {
      left: 0;
    }

    &:nth-child(2) {
      // ? Half of the flag width, to center the center of the flag to 50% mark
      margin-left: -160px;
    }

    &:last-child {
      right: 0;
      left: auto;
    }

    &:hover {
      cursor: help;

      &::after {
        position: absolute;
        bottom: -20px;

        content: attr(data-country);
      }
    }
  }
}

.flag {
  position: relative;

  width: 320px;
  height: 180px;

  .top,
  .bottom {
    position: absolute;

    width: 150px;
    height: 80px;
  }

  .bottom {
    bottom: 0;
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
      position: absolute;
      top: 0;
      left: 33.33%;

      width: 33.33%;
      height: 100%;

      &:first-child {
        left: 0;
      }
      &:last-child {
        right: 0;
        left: auto;
      }
    }
  }
}

.left {
  left: 0;
}
.right {
  right: 0;
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
