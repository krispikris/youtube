<script setup>
import { ref, onMounted } from 'vue';
import { usePage, Link } from '@inertiajs/vue3';
import MenuIcon from 'vue-material-design-icons/Menu.vue';

</script>

<template>
   
<div class="relative">
    <div id="TopNav" class="fixed flex items-center justify between w-[100%] h-[64px] bg-black z-20">
        <div class="flex items-center">
            <button class="inline-block rounded-full p-2 ml-3 hover:bg-gray-800 cursor-pointer">
                <MenuIcon fillColor="#FFFFFF" :size="26"/>
            </button>
            <div class="mx-2"></div>
            <div class="flex items-center justify-center mr-10 text-white cursor-pointer">
                YOUTUBE
            </div>
        </div>
    </div>
    <div id="SideNav"></div>
    <div id="SideNavOverlay"></div>
    <slot />
</div>
</template>
