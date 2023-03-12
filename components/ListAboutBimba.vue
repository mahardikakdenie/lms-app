<template>
  <div class="">
    <a
      href="#"
      class="flex flex-col p-3 items-center bg-white rounded-lg shadow md:flex-row md:max-w-xl hover:bg-gray-100 dark:border-gray-700 dark:bg-gray-800 dark:hover:bg-gray-700"
    >
      <img class="w-24 h-24 bg-cover mb-3 rounded-full shadow-lg" :src="item.image" width="20" alt="Bonnie image"/>
      <div class="flex flex-col justify-between p-4 leading-normal">
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          {{item.title}}
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 text-ellipsis line-clamp-3">
          {{item.description}}
        </p>
      </div>
    </a>
  </div>
</template>

<script>
export default {
    props: {
        item: {
            type: Object,
            default: () => ({}),
        },
    },
}
</script>

<style></style>
