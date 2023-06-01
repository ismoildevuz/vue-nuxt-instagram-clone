<template>
  <aside
    class="h-screen w-[250px] px-3 py-4 bg-white border-r border-r-[#DBDBDB] fixed top-0 flex flex-col justify-between"
  >
    <div>
      <div class="px-4 py-5 mt-3">
        <NuxtLink to="/">
          <img src="/icons/nav-logo.svg" alt="" />
        </NuxtLink>
      </div>

      <NuxtLink
        class="flex gap-[16px] p-4 rounded-xl font-bold hover:bg-gray-100"
        v-for="el in navLinks"
      >
        <img :src="`/icons/${el.icon}`" alt="" /> <span>{{ el.title }}</span>
      </NuxtLink>

      <NuxtLink
        class="flex gap-[16px] p-4 rounded-xl font-bold hover:bg-gray-100"
      >
        <img class="rounded-full" src="/images/nav-profile.png" alt="" />
        <span>Profile</span>
      </NuxtLink>
    </div>

    <div>
      <NuxtLink
        class="flex gap-[16px] p-4 rounded-xl font-bold hover:bg-gray-100"
      >
        <img class="rounded-full" src="/icons/nav-more.svg" alt="" />
        <span>More</span>
      </NuxtLink>
    </div>
  </aside>
</template>

<script setup>
const navLinks = [
  {
    id: 1,
    title: "Home",
    link: "/Home",
    icon: "nav-home.svg",
  },
  {
    id: 2,
    title: "Search",
    link: "/Search",
    icon: "nav-search.svg",
  },
  {
    id: 3,
    title: "Explore",
    link: "/explore",
    icon: "nav-explore.svg",
  },
  {
    id: 4,
    title: "Reels",
    link: "/reels",
    icon: "nav-reels.svg",
  },
  {
    id: 5,
    title: "Messages",
    link: "/user",
    icon: "nav-messages.svg",
  },
  {
    id: 6,
    title: "Notifications",
    link: "/chat",
    icon: "nav-notifications.svg",
  },
  {
    id: 7,
    title: "Create",
    link: "/lastest_activity",
    icon: "nav-create.svg",
  },
  // {
  //     id: 8,
  //     title: "Profile",
  //     link: "/chat",
  //     icon: "nav-profile.png"
  // },
  // {
  //     id: 9,
  //     title: "More",
  //     link: "/lastest_activity",
  //     icon: "nav-more.svg"
  // }
];
</script>

<style lang="scss" scoped></style>
