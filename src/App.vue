<template>
  <Navigation title="Junrey" :routes="routes"></Navigation>
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
    title: "Contact",
    to: "/contact",
  },
];
</script>
