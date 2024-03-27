<template>
        <q-layout view="lHh Lpr lFf">
            <q-header elevated>
            <q-toolbar>
                <q-btn flat round dense icon="menu" class="q-mr-sm" />
                <q-avatar>
                <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
                </q-avatar>
    
                <q-toolbar-title>NUXT Quasar Framework</q-toolbar-title>
    
                <q-btn flat round dense icon="whatshot" />
            </q-toolbar>
    
            <q-tabs v-model="tab">
                <q-route-tab name="images" label="Home" to="/" />
                <q-route-tab name="videos" label="About Us" to="/about" />
                <q-route-tab name="articles" label="Contact Us" to="contact-us" />
            </q-tabs>
            </q-header>
            <q-page-container class="q-pt-md" style="padding-top: 98px;">
                <slot/>
            </q-page-container>
        </q-layout>
  </template>
  <script>
  import { ref } from 'vue'
  
  export default {
    setup () {
      return {
        tab: ref('images')
      }
    }
  }
  </script>