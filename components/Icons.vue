<template>
  <div>
    <svg
      v-if="name == 'verified'"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 48 48"
      width="20"
      height="20"
    >
      <polygon
        fill="#42a5f5"
        points="29.62,3 33.053,8.308 39.367,8.624 39.686,14.937 44.997,18.367 42.116,23.995 45,29.62 39.692,33.053 39.376,39.367 33.063,39.686 29.633,44.997 24.005,42.116 18.38,45 14.947,39.692 8.633,39.376 8.314,33.063 3.003,29.633 5.884,24.005 3,18.38 8.308,14.947 8.624,8.633 14.937,8.314 18.367,3.003 23.995,5.884"
      />
      <polygon
        fill="#fff"
        points="21.396,31.255 14.899,24.76 17.021,22.639 21.428,27.046 30.996,17.772 33.084,19.926"
      />
    </svg>

    <svg
      v-else-if="name == 'arrow-left'"
      xmlns="http://www.w3.org/2000/svg"
      width="24"
      height="24"
      viewBox="0 0 24 24"
      style="fill: rgba(0, 0, 0, 1); transform: ; msfilter: "
    >
      <path
        d="M13.293 6.293 7.586 12l5.707 5.707 1.414-1.414L10.414 12l4.293-4.293z"
      ></path>
    </svg>

    <svg
      v-else-if="name == 'arrow-right'"
      xmlns="http://www.w3.org/2000/svg"
      width="24"
      height="24"
      viewBox="0 0 24 24"
      style="fill: rgba(0, 0, 0, 1); transform: ; msfilter: "
    >
      <path
        d="M10.707 17.707 16.414 12l-5.707-5.707-1.414 1.414L13.586 12l-4.293 4.293z"
      ></path>
    </svg>

    <svg
      v-else-if="name == 'arrow-right-white'"
      xmlns="http://www.w3.org/2000/svg"
      width="24"
      height="24"
      viewBox="0 0 24 24"
      style="fill: rgb(255, 255, 255) ; msfilter: "
    >
      <path
        d="M10.707 17.707 16.414 12l-5.707-5.707-1.414 1.414L13.586 12l-4.293 4.293z"
      ></path>
    </svg>

    <svg
      v-else-if="name == 'cancel'"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 50 50"
      width="20"
      height="20"
    >
      <path
        d="M 14.40625 13 L 13 14.40625 L 23.625 25 L 13 35.59375 L 14.40625 37 L 25.0625 26.40625 L 35.6875 37 L 37.09375 35.59375 L 26.46875 25 L 37.09375 14.40625 L 35.6875 13 L 25.0625 23.59375 Z"
      />
    </svg>
  </div>
</template>

<script setup>
const props = defineProps(["name", "color"]);
</script>

<style lang="scss" scoped></style>
