<script>
import { ref } from "vue";

export default {
  name: "Header",
  props: {},
  data() {
    return {
      isLoggedin: true,
    };
  },
};
</script>

<template>
  <nav
    class="w-full h-16 bg-sky-700 flex justify-between py-3 px-6 items-center"
  >
    <div>Ini Logo</div>
    <div class="flex flex-row gap-5">
      <div v-if="!isLoggedin" class="flex flex-row items-center gap-5">
        <button class="px-3 py-0.5 rounded-md bg-red-600">Login</button>
        <button class="px-3 py-0.5 rounded-md bg-white">Register</button>
      </div>
      <div v-if="isLoggedin" class="group cursor-pointer">
        <img src="" class="menu-hover w-[45px] h-[45px] rounded-full" alt="" />
        <div
          class="absolute invisible group-hover:visible bg-amber-500 rounded px-2 flex flex-col shadow-xl z-50"
        >
          <a href="#" class="text-slate-500 hover:text-black">Item 1</a>
          <a class="text-slate-500 hover:text-black">Item 2</a>
          <a class="text-slate-500 hover:text-black">Item 3</a>
        </div>
      </div>
    </div>
  </nav>
</template>
