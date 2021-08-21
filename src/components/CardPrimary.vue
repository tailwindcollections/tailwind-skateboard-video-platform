<template>
  <div
    class="h-96 rounded-2.5xl p-10 bg-no-repeat bg-cover overflow-hidden relative"
    :style="`background-image : url('${content.background}')`"
    :class="index === 0 ? 'w-2/3' : 'w-1/3'"
  >
    <h3 class="text-3xl font-semibold max-w-xxs">{{ content.title }}</h3>
    <div class="flex flex-wrap-reverse items-center pt-4 pr-24">
      <div class="relative flex items-center justify-center rounded-full w-14 h-14">
        <img class="w-12 h-12 rounded-full" :src="content.avatar" alt="" />
        <span class="absolute inset-0 border rounded-full border-white/50" />
        <component :is="content.check_icon" class="absolute bottom-0 right-0" />
      </div>
      <div class="flex flex-col py-4 pl-2">
        <a class="font-medium tracking-wider" href="#"> {{ content.name }} </a>
        <span class="text-xs tracking-wider text-white/80">
          {{ content.views }} • {{ content.created_at }}
        </span>
      </div>
    </div>
    <span
      class="px-2 py-0.5 absolute right-5 bottom-5 rounded-lg bg-gray-900/50 text-xxs"
    >
      {{ content.duration }}
    </span>
  </div>
</template>

<script>
import CheckTealIcon from "../icons/check-teal.svg";
import CheckOrangeIcon from "../icons/check-orange.svg";
export default {
  components: {
    CheckTealIcon,
    CheckOrangeIcon,
  },
  props: {
    content: {
      type: Object,
      required: true,
    },
    index: {
      type: Number,
      required: true,
    },
  },
};
</script>
