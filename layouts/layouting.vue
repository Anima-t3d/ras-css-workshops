<template>
  <div class="wrapper">
    <nuxt />
    <footer class="footer">
      <p>Created &copy;2019</p>
      <footer-layouting />
    </footer>
  </div>
</template>

<script>
import footerLayouting from '~/components/footerLayouting'
export default {
  components: {
    footerLayouting
  }
}
</script>

<style lang="scss">

.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  min-height: 100vh;
}
.footer {
  position: sticky;
  bottom: 0;

  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;

  nav {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-evenly;

    a {
      padding: 8px;

      color: black;
    }
  }
}

html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;

  box-sizing: border-box;

  word-spacing: 1px;

  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
