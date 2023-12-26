<script setup>
import { ref, onMounted } from 'vue';
import { usePage, Link } from '@inertiajs/vue3';

</script>

<template>
   
<div class="relative">
    <div id="TopNav"></div>
    <div id="SideNav"></div>
    <div id="SideNavOverlay"></div>
    <slot />
</div>
</template>
