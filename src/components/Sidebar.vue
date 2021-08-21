<template>
  <div class="px-8 pt-2 -mt-10 divide-y divide-gray-800">
    <div v-for="group in sidebarMenu" class="py-10">
      <span class="tracking-widest text-gray-500 uppercase text-xxs">
        {{ group.label }}
      </span>
      <ul class="flex flex-col pt-5 space-y-8">
        <li v-for="menu in group.children" class="flex items-center space-x-4 group">
          <span
            class="p-2 text-gray-500 bg-gray-800 rounded-xl group-hover:text-white group-hover:bg-orange"
          >
            <component class="fill-current" :is="menu.icon" />
          </span>
          <a
            class="text-sm text-gray-500 group-hover:text-white group-hover:font-semibold"
            href="#"
          >
            {{ menu.name }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import HomeIcon from "../icons/home.svg";
import ArrowRightIcon from "../icons/arrow-right.svg";
import DownloadIcon from "../icons/download.svg";
import PaperDownloadIcon from "../icons/paper-download.svg";
import WalletIcon from "../icons/wallet.svg";
const sidebarMenu = [
  {
    label: "Menu",
    children: [
      { name: "Discover", icon: HomeIcon },
      { name: "Trending", icon: ArrowRightIcon },
      { name: "Streaming", icon: DownloadIcon },
      { name: "Playlist", icon: PaperDownloadIcon },
      { name: "Bookmark", icon: WalletIcon },
    ],
  },
  {
    label: "Category",
    children: [
      { name: "Live Stream", icon: HomeIcon },
      { name: "Tutorial", icon: ArrowRightIcon },
      { name: "Competition", icon: DownloadIcon },
      { name: "Community", icon: PaperDownloadIcon },
    ],
  },
];
export default {
  setup() {
    return {
      sidebarMenu,
    };
  },
};
</script>
