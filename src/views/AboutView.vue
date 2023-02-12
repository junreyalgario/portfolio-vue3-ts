<template>
  <div class="content about">
    <Header title="About Me" :closable="true"></Header>
    <div class="mt-5 flex align-center justify-around">
      <img :src="me" alt="" />
      <div>
        <div class="field"><span class="name">Name:</span> Junrey Algario</div>
        <div class="field">
          <span class="name">Email:</span>
          junrey.algario@gmail.com
        </div>
        <div class="field">
          <span class="name">Adress:</span>
          Tacloban City, Philippines
        </div>
        <div class="field"><span class="name">Phone:</span> 09955793279</div>
        <h3 class="color-light">
          <span class="color-primary">16</span> projects completed!
        </h3>
        <div>
          <div class="mt-3">
            <a
              href="https://github.com/junreyalgario"
              class="btn outlined info mr-1"
              target="_blank"
            >
              Github
            </a>
            <a
              href="https://www.linkedin.com/in/junrey-algario-49a90a1ab/"
              class="btn outlined info mr-1"
              target="_blank"
            >
              Linkedin
            </a>
            <a
              href="https://www.onlinejobs.ph/jobseekers/info/1175607"
              class="btn outlined info mr-1"
              target="_blank"
            >
              OnlineJobs|Ph
            </a>
            <a
              href="https://www.facebook.com/iamjun92/"
              class="btn outlined info"
              target="_blank"
            >
              Facebook
            </a>
          </div>
          <div class="mt-3">
            <a class="btn outlined light mr-1" href="/contact">Say Hello!</a>
            <a
              href="files/algario-cv.pdf"
              class="btn outlined success"
              target="_blank"
            >
              Download CV
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from "@/components/Header.vue";
import me from "@/assets/images/me.png";
</script>
