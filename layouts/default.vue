<template>
  <div class="wrapper">
    <nuxt />
    <footer class="footer">
      <p>Created &copy;2019</p>
    </footer>
  </div>
</template>

<script>
export default {
  components: {

  }
}
</script>

<style lang="scss">
$cl_primary: rgb(237, 49, 60);

body {
  background: $cl_primary;
  color: white;
}

a {
  &:link,
  &:visited,
  &:hover,
  &:active {
    color: white;
  }
}

.unavailable {
  text-decoration: line-through !important;
  cursor: not-allowed !important;
}

@import url("https://fonts.googleapis.com/css?family=Oswald|Roboto:400,700");

body {
  font-size: 14px;
  line-height: 1.5;
}

// ----------------  THE FONTS

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Oswald', sans-serif;
}

h1 {
  font-size: 2rem;

  margin-bottom: 0.5em;
}

p {
  font-family: 'Roboto', sans-serif;
  // font-size: 0.8rem;
}

// ----------------  LAYOUT

.container {
  width: 90%;
  max-width: 1024px;
  margin: 0 auto;
}

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
