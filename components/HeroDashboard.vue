<template>
  <div>
    <div
      class="flex h-[720px] overflow-hidden transition duration-300 ease-in-out"
      :style="`width: ${images.length * 100}%; transform: translateX(-${transletX}%)`"
    >
      <div
        v-for="(image, i) in images"
        :key="i"
        class="bg-cover bg-gray-100 bg-black lg:bg-center bg-right w-full"
        :style="`background-image: url(${image})`"
      ></div>
    </div>
    <div class="relative z-40 container bottom-12 md:bottom-16 mx-auto flex gap-3">
      <hr
        v-for="(image, i) in images"
        :key="i"
        :class="`border-2 w-[70px] cursor-pointer ${
          setActiveCarousel(i) ? 'border-blue-600 bg-blue-600' : 'border-white bg-white'
        } `"
        @click="setActiveImage(i)"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeImage: 'https://bimba-aiueo.com/wp-content/uploads/2022/09/PRESTASI-biMBA-1600x666.jpg',
      transletX: 0,
      images: [
        'https://images.unsplash.com/photo-1588072432836-e10032774350?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1172&q=80',
        'https://images.unsplash.com/photo-1577897113292-3b95936e5206?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1690&q=80',
        'https://images.unsplash.com/photo-1577896851231-70ef18881754?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80',
      ],
    }
  },
  mounted() {
    // this.setCarouselManualy()
  },
  methods: {
    setActiveImage(index) {
      this.transletX = (index / this.images.length) * 100
    },
    setCarouselManualy() {
      const length = this.images.length
      let index = 0;
      for (index = 0; index < length;) {
        setTimeout(() => {
          this.transletX = (index / this.images.length) * 100
          // eslint-disable-next-line no-console
          console.log('index => ', index)
          index++
        }, 1000)
      }
      if (index === length) {
        index = 0
      }
    },
    setActiveCarousel(index) {
      const transletX = (index / this.images.length) * 100
      return transletX === this.transletX
    },
  },
}
</script>

<style></style>
