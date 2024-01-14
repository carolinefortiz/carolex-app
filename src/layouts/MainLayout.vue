<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="bg-pink-4">
        <q-toolbar-title> Distribuidora Vince Beauty </q-toolbar-title>

        <div>v{{ project.version }}</div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent } from "vue";
import project from "app/package.json";

export default defineComponent({
  name: "MainLayout",
  setup() {
    return {
      project,
    };
  },
});
</script>
