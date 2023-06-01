<template>
  <div class="w-[450px] py-5 border-b border-b-[#DBDBDB]">
    <div class="flex justify-between my-3">
      <div class="flex gap-3 items-center">
        <div
          class="rounded-full overflow-hidden bg-gradient-to-r from-pink-500 via-red-500 to-yellow-500 p-[2px]"
        >
          <div class="rounded-full overflow-hidden bg-white p-[2px]">
            <div
              class="rounded-full overflow-hidden bg-white w-[32px] h-[32px] flex justify-center items-center"
            >
              <img class="h-full" :src="`/images/${post.profile}`" alt="" />
            </div>
          </div>
        </div>

        <span class="font-semibold text-[#262626]">{{ post.username }}</span>

        <div>
          <Icons name="verified" />
        </div>

        <div class="flex items-center gap-1">
          <div class="bg-[#8E8E8E] h-1 w-1 rounded-full"></div>

          <span class="text-[#8E8E8E]">{{ post.date }}</span>
        </div>
      </div>

      <div class="flex items-center justify-center">
        <img src="/icons/more.svg" alt="" />
      </div>
    </div>

    <div class="carousel rounded overflow-hidden relative">
      <div
        :class="`carousel-inner-${ind} flex duration-300 transition-transform ease-in-out`"
      >
        <div
          v-for="(el, ind) in post.photos"
          :key="ind"
          class="carousel-item flex-0 flex-shrink-0 w-full"
        >
          <img class="w-full" :src="`/images/${el.name}`" alt="" />
        </div>
      </div>

      <button
        @click="prev"
        class="carousel-prev absolute top-[50%] -translate-y-[50%] left-3 rounded-full bg-white opacity-70"
      >
        <Icons name="arrow-left" class="opacity-50" />
      </button>
      <button
        @click="next"
        class="carousel-next absolute top-[50%] -translate-y-[50%] right-3 rounded-full bg-white opacity-70"
      >
        <Icons name="arrow-right" class="opacity-50" />
      </button>

      <div class="absolute bottom-3 w-full">
        <div class="flex w-full justify-center gap-1">
          <div
            v-for="(el, ind) in post.photos"
            :key="ind"
            :class="`w-2 h-2 bg-white opacity-${
              ind == post.currentPhoto ? '100' : '70'
            } rounded-full`"
          ></div>
        </div>
      </div>
    </div>

    <div class="flex justify-between items-center py-3">
      <div class="flex gap-5 items-center">
        <div class="flex items-center justify-center">
          <img src="/icons/like.svg" alt="" />
        </div>
        <div class="flex items-center justify-center">
          <img src="/icons/comment.svg" alt="" />
        </div>
        <div class="flex items-center justify-center">
          <img src="/icons/share.svg" alt="" />
        </div>
      </div>

      <div class="flex items-center justify-center">
        <img src="/icons/save.svg" alt="" />
      </div>
    </div>

    <div>
      <h3 class="font-semibold text-[15px]">
        {{ post.likes }} <span>likes</span>
      </h3>

      <h3 class="text-[15px]">
        <span class="font-semibold">{{ post.username }}</span>
        {{ post.description }}
      </h3>

      <h3 class="font-semibold text-[15px]">See translation</h3>

      <h3 class="text-[#8E8E8E] text-[15px]">
        View all {{ post.comments }} comments
      </h3>

      <div class="flex justify-between">
        <h3 class="text-[15px]">Add a comment…</h3>

        <div class="flex items-center justify-center">
          <img src="/icons/smile.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["post", "ind"]);

const prev = () => {
  if (props.post.currentPhoto > 0) {
    props.post.currentPhoto--;
    document.querySelector(
      `.carousel-inner-${props.ind}`
    ).style.transform = `translateX(-${props.post.currentPhoto * 100}%)`;
  }
};

const next = () => {
  console.log(props.post);
  const totalItems = props.post.photos.length;
  if (props.post.currentPhoto < totalItems - 1) {
    props.post.currentPhoto++;
    document.querySelector(
      `.carousel-inner-${props.ind}`
    ).style.transform = `translateX(-${props.post.currentPhoto * 100}%)`;
  }
};
</script>

<style lang="scss" scoped></style>
