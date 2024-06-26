<script setup>
import { RouterView } from 'vue-router';
import NavbarComponent from './components/layouts/NavbarComponent.vue';
</script>

<template>
    <NavbarComponent />
    <RouterView />
</template>

<style>
@import url('@/assets/css/styles.css');
</style>
