<template>
  <section class="container">
    <div
      style="display: flex; flex-direction: column; justify-content: space-between;"
    >
      <header>
        <h1 class="title">RAS CSS Workshops</h1>
        <h2 class="subtitle">
          Welcome to the
          <a href="http://www.redairship.com">Red Airship</a> CSS Workshop
          session. This page contains the source materials for the workshop
          slides.
          <br />
          <a
            href="https://docs.google.com/presentation/d/1FJZZGoeARSWFoFlBW37XEbXDNtpol-QpIdOeKWdbits/edit?usp=sharing"
          >
            The slides can be found here.
          </a>
        </h2>
      </header>
      <main
        style="min-height: 50vh; display: flex; flex-direction: column; justify-content: center;"
      >
        <p>
          Currently there are 4 main parts, click to jump to the corresponding
          session:
        </p>
        <div>
          <ol>
            <li>
              <nuxt-link to="/kickstarter">
                RAS CSS Kickstarter workshop
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/layouting">RAS CSS Layouting workshop</nuxt-link>
            </li>
            <li class="unavailable">
              <nuxt-link to="/">
                RAS CSS CSS like clockwork (Typography and animations) workshop
              </nuxt-link>
            </li>
            <li class="unavailable">
              <nuxt-link to="/">RAS CSS and beyond workshop</nuxt-link>
            </li>
          </ol>
        </div>
      </main>
    </div>
  </section>
</template>

<script>
export default {
  components: {}
}
</script>

<style lang="scss"></style>
