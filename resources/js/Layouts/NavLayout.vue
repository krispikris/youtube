<script setup>
import { ref, onMounted } from "vue";
import { usePage, Link } from "@inertiajs/vue3";
import MenuIcon from "vue-material-design-icons/Menu.vue";
</script>

<template>
  <div class="relative">
    <div
      id="TopNav"
      class="fixed flex items-center justify between w-[100%] h-[64px] bg-black z-20"
    >
      <div class="flex items-center">
        <button
          class="inline-block rounded-full p-2 ml-3 hover:bg-gray-800 cursor-pointer"
        >
          <MenuIcon fillColor="#FFFFFF" :size="26" />
        </button>
        <div class="mx-2"></div>
        <div
          class="flex items-center justify-center mr-10 text-white cursor-pointer"
        >
          YOUTUBE
        </div>

        <div class="w-[600px] md:block hidden">
          <input
            type="text"
            class="form-control block w-full px-5 py-1.5 text-base font-normal text-gray-200 bg-black placeholder-gray-400 bg-clip-padding border border-solid border-l-gray-700 border-y-gray-900 rounded-l-full transistion ease-in-out m-0 border-transparent focus:ring-0"
          />
        </div>
      </div>
    </div>

    <div id="SideNav"></div>
    <div id="SideNavOverlay"></div>
    <slot />
  </div>
</template>
