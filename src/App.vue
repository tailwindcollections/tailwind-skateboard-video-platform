<template>
  <div class="flex font-sans text-white bg-gray-900">
    <div class="flex flex-col min-h-screen w-80">
      <div class="px-8 py-8">
        <h1 class="text-xl font-semibold">skateboard</h1>
      </div>
      <Sidebar />
    </div>

    <div class="flex flex-col w-full pl-5 pr-14 py-7">
      <Navbar />

      <div class="pt-10">
        <h2 class="text-4xl font-semibold">Discover</h2>
        <div class="flex space-x-6 py-7">
          <CardPrimary
            v-for="(card, index) in primaryCard"
            :content="card"
            :index="index"
          />
        </div>
      </div>

      <div class="pt-4">
        <h2 class="text-2xl font-medium">Most watched</h2>
        <div class="flex justify-between py-6">
          <CardSecondary v-for="card in secondaryCard" :content="card" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CardSecondary from "./components/CardSecondary.vue";
import CardPrimary from "./components/CardPrimary.vue";
import Navbar from "./components/Navbar.vue";
import Sidebar from "./components/Sidebar.vue";

const primaryCard = [
  {
    title: "How to do Basic Jumping and how to landing safely",
    avatar: "/img/avatar-3.png",
    background: "/img/bg-1.png",
    name: "Thomas Hope",
    views: "53K views",
    created_at: "2 weeks ago",
    check_icon: "CheckTealIcon",
    duration: "7 min",
  },
  {
    title: "Skateboard Tips You need to know",
    avatar: "/img/avatar-2.png",
    background: "/img/bg-2.png",
    name: "Tony Andrew",
    views: "52K views",
    created_at: "1 weeks ago",
    check_icon: "CheckOrangeIcon",
    duration: "10 min",
  },
];

const secondaryCard = [
  {
    title: "Basic how to ride your skateboard comfortly",
    avatar: "/img/avatar-6.png",
    background: "/img/bg-3.png",
    name: "Andy William",
    views: "53K views",
    created_at: "2 weeks ago",
    color: "green",
    duration: "7 min",
  },
  {
    title: "Prepare for your first skateboard jump",
    avatar: "/img/avatar-4.png",
    background: "/img/bg-7.png",
    name: "Johny Wise",
    views: "53K views",
    created_at: "2 weeks ago",
    color: "orange",
    duration: "7 min",
  },
  {
    title: "Tips to playing skateboard on the ramp",
    avatar: "/img/avatar-8.png",
    background: "/img/bg-6.png",
    name: "Budi Hakim",
    views: "53K views",
    created_at: "2 weeks ago",
    color: "orange",
    duration: "7 min",
  },
  {
    title: "Basic Equipment to play skateboard safely",
    avatar: "/img/avatar-7.png",
    background: "/img/bg-4.png",
    name: "Wijaya Abadi",
    views: "53K views",
    created_at: "2 weeks ago",
    color: "green",
    duration: "7 min",
  },
];
export default {
  components: { Sidebar, Navbar, CardPrimary, CardSecondary },
  setup() {
    return {
      primaryCard,
      secondaryCard,
    };
  },
};
</script>
