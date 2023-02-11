<template>
  <nav class="navigation">
    <div class="desktop">
      <div class="title">{{ props.title }}</div>
      <div>
        <ul class="desktop">
          <li
            :class="{ active: path === route.to }"
            v-for="(route, index) in props.routes"
            :key="index"
          >
            <router-link :to="route.to">{{ route.title }}</router-link>
          </li>
        </ul>
      </div>
      <button class="menu" @click="menuClick">
        <font-awesome-icon class="icon light" icon="fa-solid fa-bars" />
      </button>
    </div>
    <div class="mobile">
      <ul v-if="state.menu">
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
import { defineProps, PropType, computed, reactive } from "vue";
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

const state = reactive({ menu: false });
const route = useRoute();
const path = computed(() => route.path);

const menuClick = () => {
  state.menu = !state.menu;
};
</script>
