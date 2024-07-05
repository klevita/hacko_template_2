<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar color="white" class="q-ma-xs">
        <q-toolbar-title>Quasar App</q-toolbar-title>
        <q-btn @click="logout(); $router.push({name: 'Login'})" flat round color="white" size="md" icon="logout" />
      </q-toolbar>
    </q-header>
    <q-page-container>
      <q-page class="background">
        <router-view />
      </q-page>
    </q-page-container>
  </q-layout>
</template>
<script setup lang="ts">
import { useUserStore } from 'src/stores/UserStore'

const { logout } = useUserStore()
</script>
