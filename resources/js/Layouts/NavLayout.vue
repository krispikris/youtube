<script setup>
import { ref, onMounted } from "vue";
import { usePage, Link } from "@inertiajs/vue3";
import MenuIcon from "vue-material-design-icons/Menu.vue";
import MagnifyIcon from "vue-material-design-icons/Magnify.vue";
import SideNavItem from "@/Components/SideNavItem.vue";

let openSideNav = ref(true);
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
          <div class="flex items-center rounded-full bg-[#222222]">
            <input
              type="text"
              class="
                      block
                      form-control
                      w-full
                      m-0
                      px-5
                      py-1.5
                      text-base
                      font-normal
                      text-gray-200
                      bg-black
                      placeholder-gray-400
                      bg-clip-padding
                      border
                      border-solid
                      border-l-gray-700
                      border-y-gray-700
                      rounded-l-full
                      transition
                      ease-in-out
                      border-transparent
                      focus:ring-0"
              placeholder="Search"
            />
            <MagnifyIcon class="mx-6" fillColor="#FFFFFF" :size="23"/>
          </div>
        </div>
        <div>
          <img
            class="rounded-full mx-8"
            width="36"
            src="https://yt3.ggpht.com/ytc/AIf8zZSTSt4eDvtstqNGA6fyHmC6T_j75F9A7E5vnjESJkhtGBUzrdvUBgnlTmYD-hKq=s88-c-k-c0x00ffffff-no-rj"
          >
        </div>
      </div>
    </div>

    <div id="SideNav" class="fixed w-[240px] h-[100%] bg-black">
        <ul class="w-full mt-[64px]">
            <SideNavItem :openSideNav="openSideNav" iconString="Home"/>
        </ul>
    </div>

    <div id="SideNavOverlay"></div>
    <slot />
  </div>
</template>
