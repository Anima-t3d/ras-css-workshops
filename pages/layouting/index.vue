<template>
  <section class="container">
    <div>
      <h1 class="title">Layouting in CSS</h1>
      <h2 class="subtitle">
        Below is a timeline of different ways a webdeveloper can use HTML and
        CSS to style and position elements on a page. I added an example for
        each, using flags.
      </h2>

      <div style="margin-left: 4px; margin-top: 8px;">
        <div class="timeline-item" date-is="24-11-1995">
          <h1 id="table">
            <nuxt-link to="/layouting/table">Table</nuxt-link>
          </h1>
          <p>
            The HTML
            <code>&lt;table&gt;</code> element represents tabular data — that
            is, information presented in a two-dimensional table comprised of
            rows and columns of cells containing data.
          </p>
          <p>
            Introduced in
            <a href="https://tools.ietf.org/html/rfc1942">HTML 2.0 RFC</a>
            also see
            <a href="https://www.w3.org/TR/html401/struct/tables.html"
              >HTML 4.01</a
            >
          </p>
          <p>
            <a
              href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table"
              >MDN Source</a
            >
          </p>
          <p>
            <strong>Example:</strong>
            <nuxt-link to="/layouting/table">Table</nuxt-link>
          </p>
        </div>
        <div class="timeline-item" date-is="17-12-1996">
          <h1 id="floats">
            <nuxt-link to="/layouting/floats">Floats</nuxt-link>
          </h1>
          <p>
            The <code>float</code> CSS property places an element on the left or
            right side of its container, allowing text and inline elements to
            wrap around it. The element is removed from the normal flow of the
            page, though still remaining a part of the flow (in contrast to
            absolute positioning).
          </p>
          <p>
            Introduced in
            <a href="https://www.w3.org/TR/CSS1/#floating-elements"
              >CSS Level 1</a
            >
          </p>
          <p>
            <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/float"
              >MDN Source</a
            >
          </p>
          <p>
            <strong>Example:</strong>
            <nuxt-link to="/layouting/floats">Floats</nuxt-link>
          </p>
        </div>

        <div class="timeline-item" date-is="12-05-1998">
          <h1 id="positioning">
            <nuxt-link to="/layouting/positioning">Positioning</nuxt-link>
          </h1>
          <p>
            The <code>position</code> CSS property sets how an element is
            positioned in a document. The <code>top</code>, <code>right</code>,
            <code>bottom</code>, and <code>left</code>
            properties determine the final location of positioned elements.
          </p>
          <p>
            Introduced in
            <a
              href="https://www.w3.org/TR/2008/REC-CSS2-20080411/visuren.html#positioning-scheme"
              >CSS Level 2</a
            >
          </p>
          <p>
            <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/position"
              >MDN Source</a
            >
          </p>
          <p>
            <strong>Example:</strong>
            <nuxt-link to="/layouting/positioning">Positioning</nuxt-link>
          </p>
        </div>

        <div class="timeline-item" date-is="19-11-2018">
          <h1 id="flex">
            <nuxt-link to="/layouting/flex">Flex</nuxt-link>
          </h1>
          <p>
            The <code>flex</code> CSS property sets how a flex item will grow or
            shrink to fit the space available in its flex container. It is a
            shorthand for <code>flex-grow</code>, <code>flex-shrink</code>, and
            <code>flex-basis</code>.
          </p>
          <p>
            Introduced in
            <a href="https://www.w3.org/TR/css-flexbox-1/#intro"
              >CSS Level 3 / CSS Flexible Box Layout Module Level 1</a
            >
          </p>
          <p>
            <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/flex"
              >MDN Source</a
            >
            also see
            <a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox/"
              >CSS Tricks Flex guide</a
            >
          </p>
          <p>
            <strong>Example:</strong>
            <nuxt-link to="/layouting/flex">Flex</nuxt-link>
          </p>
        </div>

        <div class="timeline-item" date-is="??-??-????">
          <h1 id="grid">
            <nuxt-link to="/layouting/grid">Grid</nuxt-link>
          </h1>
          <p>
            CSS Grid Layout excels at dividing a page into major regions or
            defining the relationship in terms of size, position, and layer,
            between parts of a control built from HTML primitives.
          </p>
          <p>
            Like tables, grid layout enables an author to align elements into
            columns and rows. However, many more layouts are either possible or
            easier with CSS grid than they were with tables. For example, a grid
            container's child elements could position themselves so they
            actually overlap and layer, similar to CSS positioned elements.
          </p>
          <p>
            Introduced in
            <a href="https://www.w3.org/TR/css-grid-2/"
              >CSS Grid Layout Module Level 2 Working Draft</a
            >
          </p>
          <p>
            <a
              href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout"
              >MDN Source</a
            >
            also see
            <a href="https://css-tricks.com/snippets/css/complete-guide-grid/"
              >CSS Tricks Grid guide</a
            >
          </p>
          <p>
            <strong>Example:</strong>
            <nuxt-link to="/layouting/grid">Grid</nuxt-link>
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  components: {}
}
</script>

<style lang="scss" scoped>
/* Timeline: https://codepen.io/NielsVoogt/pen/MbMMxv/ */
@import url('https://fonts.googleapis.com/css?family=Oswald|Roboto:400,700');

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
  font-size: 0.8rem;
}

// ----------------  LAYOUT

/* .container {
  // width: 90%;
  // max-width: 1024px;
  // margin: 0 auto;

} */

// ----------------  THE FONTS

$border-color: rgba(black, 0.3);

.timeline-item {
  position: relative;

  padding: 3em 2em 2em;

  color: rgba(white, 0.7);
  border-left: 2px solid $border-color;

  p {
    font-size: 1rem;
  }

  &::before {
    font-family: 'Roboto', sans-serif;
    font-size: 0.785rem;
    font-weight: bold;
    font-weight: 700;

    position: absolute;
    top: 0.8em;
    left: 2em;

    display: block;

    content: attr(date-is);
  }

  &::after {
    position: absolute;
    top: 1em;
    left: -7px;

    display: block;

    width: 10px;
    height: 10px;

    content: '';

    border: 2px solid $border-color;
    border-radius: 10px;
    background: white;
  }

  &:last-child {
    border-image: linear-gradient(
        to bottom,
        $border-color 60%,
        rgba($border-color, 0)
      )
      1 100%;
  }
}
</style>
