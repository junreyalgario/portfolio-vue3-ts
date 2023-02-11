<template>
  <div class="header">
    <h1 class="title">{{ props.title }}</h1>
    <button v-if="props.closable" class="icon close">
      <font-awesome-icon class="icon" icon="fa-solid fa-close" @click="close" />
    </button>
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits } from "vue";
import router from "@/router";

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  closable: {
    type: Boolean,
    default: false,
    required: false,
  },
});

const emit = defineEmits(["close"]);

const close = () => {
  router.go(-1);
  emit("close");
};
</script>
