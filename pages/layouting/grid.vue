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
  name: 'Grid',
  layout: 'layouting',
}
</script>

<style lang="scss" scoped>
.flags {
  display: grid;

  grid-template-columns: [flag-1] 320px [void-1] auto [flag-2] 320px [void-2] auto [flag-3] 320px;

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
  display: grid;

  width: 320px;
  height: 180px;

  &:nth-child(1) {
    grid-column-start: flag-1;
  }

  &:nth-child(2) {
    grid-column-start: flag-2;
  }

  &:nth-child(3) {
    grid-column-start: flag-3;
    grid-template-rows: 80px auto 80px;
    grid-template-columns: 100px auto 200px;
  }

  .top {
    grid-column-start: 1;
  }

  .bottom {
    grid-column-start: 3;
  }

  .left {
    grid-row-start: 1;
  }

  .right {
    grid-row-start: 3;
  }
}
.stripes-3 {
  grid-template-rows: repeat(3, 1fr);
  grid-template-columns: repeat(3, 1fr);

  > div {
    grid-row-start: 1;
    grid-column: span 3;

    &:nth-child(2) {
      grid-row-start: 2;
    }

    &:nth-child(3) {
      grid-row-start: 3;
    }
  }
  &.vertical {
    > div {
      grid-column-start: 1;
      grid-row-start: 1;
      grid-row-end: span 3;

      &:nth-child(2) {
        grid-column-start: 2;
      }

      &:nth-child(3) {
        grid-column-start: 3;
      }
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
