<template>
  <div class="content home">
    <div>
      <span class="color-primary">Hello!</span>
      <h1>I'm <span class="highlight">JUNREY ALGARIO</span></h1>
      <div class="text">
        <h2>
          A full-stack
          <span class="highlight">Web</span>,
          <span class="highlight">Android</span>
          and
          <span class="highlight">Flutter</span>
          Developer
        </h2>
        <h2>
          I'm a
          <span class="highlight">Software Developer</span>
          based in the
          <span class="highlight">Philippines</span>
        </h2>
      </div>
      <div class="mt-4">
        <a class="btn outlined light mr-1" href="/contact">Say Hello!</a>
        <a class="btn outlined success mr-1" href="#">My Works</a>
        <a
          class="btn info outlined"
          href="https://github.com/junreyalgario"
          target="_blank"
        >
          Follow on Github
        </a>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from "vue";

onMounted(() => {
  console.log("On mounted");
});
</script>
