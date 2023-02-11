<template>
  <nav class="header">
    <div>{{ props.title }}</div>
    <div class="r-list">
      <ul>
        <li v-for="(route, index) in props.routes" :key="index">
          <router-link :to="route.to">{{ route.title }}</router-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { defineProps, PropType } from "vue";
import { Route } from "@/types";

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  routes: {
    type: Object as PropType<Array<Route>>,
    required: true,
  },
});
</script>
