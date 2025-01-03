<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title> {KIQ} </q-toolbar-title>

        <q-btn stretch flat label="Inicio" />
        <q-btn stretch flat label="Sobre" />
        <q-btn stretch flat label="Habilidades" />
        <q-icon name="light_mode" @click="toggleDarkMode" size="1.4rem" />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style></style>

<script setup>
import { useQuasar } from 'quasar'

const $q = useQuasar()
// get status
console.log($q.dark.isActive) // true, false
// get configured status
console.log($q.dark.mode) // "auto", true, false
// set status
$q.dark.set(true) // or false or "auto"
// toggle
function toggleDarkMode() {
  $q.dark.toggle()
}
</script>
