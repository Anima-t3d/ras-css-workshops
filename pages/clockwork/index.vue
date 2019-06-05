<template>
  <div>
    <div class="clock round">
      <div class="face">
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
      </div>
      <div class="hand hour"></div>
      <div class="hand minute"></div>
      <div class="hand second"></div>
    </div>

    <div class="clock square">
      <div class="face">
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
        <div class="markers"></div>
      </div>
      <div class="hand hour"></div>
      <div class="hand minute"></div>
      <div class="hand second"></div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.clock {
  position: relative;

  width: 160px;
  height: 160px;

  &.round {
    border: 4px solid orange;
    border-radius: 50%;
  }

  &.square {
    padding: 16px;

    border-image: url(https://mdn.mozillademos.org/files/6017/border-image-6.svg) 42 fill / 42px / 0 round;

    .hour {
      &::after {
        height: 40px;
      }
    }

    .minute {
      &::after {
        height: 30px;
      }
    }

    .second {
      &::after {
        height: 40px;
      }
    }

    .markers {
      width: 100px;
      margin-left: -50px;
    }
  }
}

.hand {
  position: absolute;
  top: 50%;
  left: 50%;

  width: 16px;
  height: 16px;
  margin-top: -8px;
  margin-left: -8px;

  border-radius: 50%;
  background: maroon;
}

.hour,
.minute,
.second {
  &::after {
    position: absolute;
    bottom: 0;

    width: 4px;
    height: 60px;
    margin-bottom: 6px;
    margin-left: 6px;

    content: "";
    transform-origin: bottom center;
    animation: ticktock 43200s infinite steps(12);

    background: maroon;
  }
}

.minute {
  &::after {
    height: 30px;

    animation: ticktock 3600s infinite steps(60);

    background: orange;
  }
}

.second {
  &::after {
    width: 2px;

    animation: ticktock 60s infinite steps(60);

    background: coral;
  }
}

@keyframes ticktock {
  100% {
    transform: rotate(360deg);
  }
}

.face {
  padding: 8px;

  .markers {
    position: absolute;
    top: 50%;
    left: 50%;

    width: 100%;
    height: 4px;
    margin-top: -4px;
    margin-left: -50%;

    transform: rotate(30deg) translate(4px, 50%);
    transform-origin: center bottom;

    &:nth-child(1) {
      transform: rotate(30deg) translate(4px, 50%);
    }

    &:nth-child(2) {
      transform: rotate(60deg) translate(4px, 50%);
    }

    &:nth-child(3) {
      transform: rotate(90deg) translate(4px, 50%);
    }

    &:nth-child(4) {
      transform: rotate(120deg) translate(4px, 50%);
    }

    &:nth-child(5) {
      transform: rotate(150deg) translate(4px, 50%);
    }

    &:nth-child(6) {
      transform: rotate(180deg) translate(4px, 50%);
    }

    &::after,
    &::before {
      position: absolute;
      left: -4px;

      width: 8px;
      height: 4px;

      content: "";

      background: maroon;
    }

    &::after {
      right: 5px;
      left: auto;
    }
  }
}
</style>
