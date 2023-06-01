<template>
  <div class="min-h-screen w-full">
    <div class="bg-slate-300 h-[100px]"></div>

    <div class="flex justify-center">
      <div>
        <PostCard
          v-for="(el, ind) in posts.slice(0, 2)"
          :key="ind"
          :post="el"
          :ind="ind"
        />

        <Suggestions />

        <PostCard
          v-for="(el, ind) in posts.slice(2)"
          :key="ind + 2"
          :post="el"
          :ind="ind + 2"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
const posts = ref([
  {
    profile: "post-profile.png",
    username: "lewishamilton",
    date: "5h",
    likes: 465132,
    comments: 64465,
    description: "Parabéns Ayrton, minha inspiração sempre 💫",
    photos: [
      {
        name: "post-image.png",
      },
      {
        name: "post-image.png",
      },
      {
        name: "post-image.png",
      },
      {
        name: "post-image.png",
      },
    ],
    currentPhoto: 0,
  },
  {
    profile: "post-profile-2.png",
    username: "kurzgesagt",
    date: "8h",
    likes: 5132,
    comments: 65,
    description:
      "For every video we upload to YouTube we create different versions of the final thumbnail.",
    photos: [
      {
        name: "post-image-2.png",
      },
      {
        name: "post-image-2.png",
      },
      {
        name: "post-image-2.png",
      },
      {
        name: "post-image-2.png",
      },
    ],
    currentPhoto: 0,
  },
  {
    profile: "post-profile-3.png",
    username: "discovery",
    date: "2d",
    likes: 65132,
    comments: 465,
    description:
      "If you had to choose, where would you be the fastest: air, land, or sea?",
    photos: [
      {
        name: "post-image-3.png",
      },
      {
        name: "post-image-3.png",
      },
      {
        name: "post-image-3.png",
      },
      {
        name: "post-image-3.png",
      },
    ],
    currentPhoto: 0,
  },
]);
</script>

<style lang="scss" scoped></style>
