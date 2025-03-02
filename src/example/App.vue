<script setup lang="ts">
import { CommonProvider, defineProvider } from "../index";
import {
  NModalProvider,
  NConfigProvider,
  NMessageProvider,
  darkTheme,
} from "naive-ui";
import ComponentA from "./ComponentA.vue";

const providers = [
  defineProvider(NConfigProvider, {
    theme: darkTheme,
    tag:"section"
  }),
  defineProvider(NModalProvider),
  defineProvider(NMessageProvider),
];
</script>
<template>
  <div>
    <CommonProvider :providers="providers">
      <ComponentA></ComponentA>
    </CommonProvider>
  </div>
</template>
