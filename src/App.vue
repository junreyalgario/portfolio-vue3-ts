<template>
  <Navigation title="JUNREY" :routes="routes"></Navigation>
  <router-view />
</template>

<script setup lang="ts">
import Navigation from "@/components/Navigation.vue";
import { Route } from "./types";

const routes: Array<Route> = [
  {
    title: "Home",
    to: "/",
  },
  {
    title: "About",
    to: "/about",
  },
  {
    title: "Resume",
    to: "/resume",
  },
  {
    title: "Services",
    to: "/services",
  },
  {
    title: "Skills",
    to: "/skills",
  },
  {
    title: "Portfolio",
    to: "/portfolio",
  },
  {
    title: "Contact",
    to: "/contact",
  },
];
</script>
