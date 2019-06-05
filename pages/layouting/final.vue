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
    <div class="flag blue" data-country="United Kingdom">
      <div class="flag__content">
        <div class="white diagonal"></div>
        <div class="white diagonal ccw"></div>
        <div class="red diagonal top"></div>
        <div class="red diagonal top ccw"></div>
        <div class="red diagonal bottom"></div>
        <div class="red diagonal bottom ccw"></div>
        <div class="white vertical"></div>
        <div class="white horizontal"></div>
        <div class="red vertical"></div>
        <div class="red horizontal"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Final',
  layout: 'layouting',
}
</script>

<style lang="scss" scoped>
.flags {
  display: grid;

  grid-template-columns: [flag-1] 320px [void-1] auto [flag-2] 320px [void-2] auto [flag-3] 320px;
  grid-template-rows: [flag-row-1] 180px [void-1] 180px [flag-row-2] 180px [void-2] 180px [flag-row-3] 180px;

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

  &[data-country="United Kingdom"] {
    grid-column-start: flag-2;
    grid-row-start: flag-row-2;

    .flag__content {
      position: relative;

      display: block;
      overflow: hidden;

      width: 100%;
      height: 100%;

      > div {
        position: absolute;
        top: 50%;
        left: 0;

        width: 100%;
        height: 30px;

        transform-origin: center;
      }

      .horizontal {
        margin-top: -15px;
        &.white {
          height: 50px;
          margin-top: -25px;
        }
      }

      .vertical {
        transform: rotate(90deg);

        &.white {
          height: 50px;
        }
      }

      .diagonal {
        left: -30px;

        width: 380px;
        height: 10px;

        transform: rotate(30deg);

        &.white {
          height: 30px;
          margin-top: -15px;
        }
        &.red {
          top: 86px;
          left: -50px;

          width: 200px;
          margin-top: 0;

          transform-origin: right;

          &.bottom {
            top: 10px;
            top: 50%;
            left: 0;
            left: 50%;

            margin-top: -11px;

            transform-origin: left;
          }
        }

        &.ccw {
          transform: rotate(-30deg);

          &.red {
            top: -13px;
            right: 0;
            left: auto;
            &.bottom {
              top: 195px;
              left: 0;

              transform-origin: left;
            }
          }
        }
      }
    }
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
.white {
  background-color: white;
}
</style>
