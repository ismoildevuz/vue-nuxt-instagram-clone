<template>
  <aside class="h-screen w-[450px] flex-shrink-0 p-10 pr-[100px]">
    <div class="flex">
      <img class="rounded-full" src="/images/profile.png" alt="" />

      <div class="ml-[18px] w-full text-[14px] mt-[7px]">
        <p class="font-bold">{{ profile.username }}</p>
        <p class="text-[#8E8E8E]">{{ profile.fullname }}</p>
      </div>

      <p class="text-[#0095F6] text-[12px] flex items-center font-semibold">
        Switch
      </p>
    </div>

    <div class="w-full mt-[15px]">
      <div class="flex justify-between ml-[-4px]">
        <p class="text-[14px] text-[#8E8E8E] font-semibold">
          Suggestions for you
        </p>
        <p class="text-[11px] font-bold flex items-center">See All</p>
      </div>
      <div class="mt-[8px]">
        <div
          v-for="(el, ind) in profiles.slice(0, 5)"
          :key="ind"
          class="flex items-center w-full justify-between"
        >
          <img
            class="rounded-full w-[32px] h-[32px]"
            :src="`/images/${el.image}`"
            alt=""
          />
          <div class="ml-[18px] w-[209px] text-[14px] mt-[7px]">
            <p class="font-bold text-[14px]">{{ el.username }}</p>
            <p class="text-[#8E8E8E] text-[12px]">{{ el.info }}</p>
          </div>
          <p class="text-[#0095F6] text-[12px] flex items-center font-bold">
            Follow
          </p>
        </div>
      </div>
    </div>

    <div class="w-[319px] text-[#C7C7C7] text-[12px] mt-[23px]">
      <div class="flex gap-[3px] w-[319px]">
        <p>About</p>
        <p>Help</p>
        <p>Press</p>
        <p>API</p>
        <p>Jobs</p>
        <p>Privacy</p>
        <p>Terms</p>
        <p>Locations</p>
      </div>

      <div class="flex mt-[2px]">
        <p>Language</p>
        <p>Meta Verified</p>
      </div>

      <div class="mt-[21px]">
        <p>© 2023 INSTAGRAM FROM META</p>
      </div>
    </div>
  </aside>
</template>

<script setup>
const profile = reactive({
  username: "upvox_",
  fullname: "Upvox",
});

const profiles = ref([
  {
    id: 1,
    image: "side-profile-1.png",
    username: "imkirtichadha",
    info: "Follows you",
  },
  {
    id: 2,
    image: "side-profile-2.png",
    username: "organic__algorithm",
    info: "Followed by chirag_singla17",
  },
  {
    id: 3,
    image: "side-profile-3.png",
    username: "im_grohit",
    info: "Follows you",
  },
  {
    id: 4,
    image: "side-profile-4.png",
    username: "saurabh952",
    info: "Followed by chirag_singla17",
  },
  {
    id: 5,
    image: "side-profile-5.png",
    username: "sarthakbrl",
    info: "Follows you",
  },
  {
    id: 6,
    image: "side-profile-1.png",
    username: "imkirtichadha",
    info: "Followed by chirag_singla17",
  },
  {
    id: 7,
    image: "side-profile-2.png",
    username: "organic__algorithm",
    info: "Follows you",
  },
  {
    id: 8,
    image: "side-profile-3.png",
    username: "im_grohit",
    info: "Followed by chirag_singla17",
  },
  {
    id: 9,
    image: "side-profile-4.png",
    username: "saurabh952",
    info: "Follows you",
  },
  {
    id: 10,
    image: "side-profile-5.png",
    username: "sarthakbrl",
    info: "Followed by chirag_singla17",
  },
]);
</script>

<style lang="scss" scoped></style>
