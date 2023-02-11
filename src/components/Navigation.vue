<template>
  <nav class="header">
    <div class="title">{{ props.title }}</div>
    <div class="r-list">
      <ul>
        <li
          :class="{ active: path === route.to }"
          v-for="(route, index) in props.routes"
          :key="index"
        >
          <router-link :to="route.to">{{ route.title }}</router-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { defineProps, PropType, reactive, watch, computed } from "vue";
import { useRoute } from "vue-router";
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

const route = useRoute();
const path = computed(() => route.path);
</script>
