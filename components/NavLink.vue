<template>
  <li class="w-full">
    <a
      class="
      md:px-4 py-2 text-sm bg-transparent rounded-lg text-[#666666]
      focus:outline-none focus:shadow-outline whitespace-nowrap cursor-pointer font-bold
      hover:text-blue-400 hover:border-b-2 hover:border-b-blue-400 hover:rounded-none
      "
      :class="{'text-blue-600 border-b-2 rounded-none border-b-blue-600': url === $route.path }"
      @click="$router.push(url)"
    >
      {{ name }}
    </a>
  </li>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
  },
}
</script>
