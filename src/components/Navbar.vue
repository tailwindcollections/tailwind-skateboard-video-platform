<template>
  <div class="flex items-center justify-between">
    <div class="relative flex flex-1 max-w-xl">
      <input
        class="items-center w-full h-10 px-4 text-sm font-normal tracking-wider text-white placeholder-gray-500 bg-white/10 rounded-xl focus:outline-none"
        type="text"
        placeholder="Search"
      />
      <div class="absolute inset-y-0 right-0 flex items-center pr-6">
        <SearchIcon class="text-gray-500 stroke-current" />
      </div>
    </div>
    <div class="flex items-center">
      <img class="w-8 h-8 rounded-full" src="/img/avatar-1.png" alt="" />
      <a class="inline-flex items-center pl-4" href="#">
        <span class="text-xs font-normal tracking-widest">Thomas</span>
        <ChevronDownIcon class="text-gray-500 fill-current" />
      </a>
      <button class="pl-8 p-0.5 relative">
        <NotificationIcon class="text-gray-500 fill-current" />
        <span
          class="absolute top-0 w-2 h-2 bg-red-500 border border-gray-900 rounded-full right-1"
        ></span>
      </button>
    </div>
  </div>
</template>

<script>
import SearchIcon from "../icons/search.svg";
import ChevronDownIcon from "../icons/chevron-down.svg";
import NotificationIcon from "../icons/notification.svg";

export default {
  components: {
    SearchIcon,
    ChevronDownIcon,
    NotificationIcon,
  },
};
</script>
