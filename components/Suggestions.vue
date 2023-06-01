<template>
  <div class="w-[450px] py-5 border-b border-b-[#DBDBDB] overflow-hidden">
    <div class="flex justify-between font-semibold">
      <div>
        <h2 class="text-[#8E8E8E] text-[15px]">Suggestions for you</h2>
      </div>

      <div>
        <h2 class="text-[#0095F6] text-[15px]">See all</h2>
      </div>
    </div>

    <div class="relative my-5">
      <button
        class="absolute top-[50%] -translate-y-[50%] z-10 right-3 rounded-full overflow-hidden bg-gray-500 opacity-90"
      >
        <Icons name="arrow-right-white" />
      </button>

      <div class="flex gap-5">
        <div v-for="(el, ind) in suggestions" :key="ind">
          <div
            class="w-[160px] h-[180px] border border-[#DBDBDB] rounded relative p-3 flex flex-col justify-between items-center"
          >
            <button
              class="absolute top-3 right-3 rounded-full hover:bg-slate-50 p-1"
            >
              <Icons name="cancel" />
            </button>

            <div class="w-[50px] h-[50px] rounded-full overflow-hidden">
              <img :src="`/images/${el.image}`" alt="" />
            </div>

            <div class="text-center text-[10px]">
              <h3>{{ el.fullname }}</h3>
              <h3 class="text-[#8E8E8E]">{{ el.info }}</h3>
            </div>

            <button
              class="rounded-lg bg-[#0095F6] py-2 px-5 text-white text-[12px] font-semibold"
            >
              <span> Follow </span>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const suggestions = ref([
  {
    id: 1,
    image: "suggestion-profile.png",
    fullname: "Kirti Chadha",
    info: "Follows you",
  },
  {
    id: 2,
    image: "suggestion-profile-2.png",
    fullname: "Durgesh Nandini",
    info: "Followed by chirag_singla17",
  },
  {
    id: 3,
    image: "suggestion-profile.png",
    fullname: "Kirti Chadha",
    info: "Follows you",
  },
  {
    id: 4,
    image: "suggestion-profile-2.png",
    fullname: "Durgesh Nandini",
    info: "Followed by chirag_singla17",
  },
  {
    id: 5,
    image: "suggestion-profile.png",
    fullname: "Kirti Chadha",
    info: "Follows you",
  },
  {
    id: 6,
    image: "suggestion-profile-2.png",
    fullname: "Durgesh Nandini",
    info: "Followed by chirag_singla17",
  },
  {
    id: 7,
    image: "suggestion-profile.png",
    fullname: "Kirti Chadha",
    info: "Follows you",
  },
  {
    id: 8,
    image: "suggestion-profile-2.png",
    fullname: "Durgesh Nandini",
    info: "Followed by chirag_singla17",
  },
  {
    id: 9,
    image: "suggestion-profile.png",
    fullname: "Kirti Chadha",
    info: "Follows you",
  },
  {
    id: 10,
    image: "suggestion-profile-2.png",
    fullname: "Durgesh Nandini",
    info: "Followed by chirag_singla17",
  },
]);
</script>

<style lang="scss" scoped></style>
