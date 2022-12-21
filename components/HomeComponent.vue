<template>
  <div id="app">
    <div class="reveal">
      <div class="slides">
        <section data-markdown>
          <textarea data-template>
            # Slide 1
            > A paragraph with some text and a [link](http://hakim.se).
          </textarea>
        </section>
        <section data-markdown>
          <textarea data-template>
            ```js [1-2|3|4]
            let a = 1;
            let b = 2;
            let c = x => 1 + 2 + x;
            c(3);
            ```
          </textarea>
        </section>
        <section>Slide 1</section>
        <section>Slide 2</section>
      </div>
    </div>
  </div>
</template>

<script>
import Reveal from "reveal.js";
import "reveal.js/plugin/highlight/monokai.css";
import Markdown from "reveal.js/plugin/markdown/markdown.js";
import Highlight from "reveal.js/plugin/highlight/highlight";
export default {
  mounted() {
    Reveal.initialize({
      plugins: [Markdown, Highlight],
      markdown: {
        breaks: true,
        gfm: true,
      },
    });
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  height: 90vh;
}
</style>
