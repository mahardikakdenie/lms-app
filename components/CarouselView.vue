<template>
    <div>
        <div
            class="flex h-[400px] rounded shadow-md overflow-hidden transition duration-300 ease-in-out"
            :style="`width: ${imgs.length * 100}%; transform: translateX(-${transletX}%)`"
        >
            <div
                v-for="(img, i) in imgs"
                :key="i"
                class="bg-cover bg-gray-100 bg-black lg:bg-center bg-right w-full opacity-80"
                :style="`background-image: url(${img})`"
            ></div>
        </div>
        <div class="relative z-40 p-6 container bottom-12 md:bottom-16 mx-auto flex gap-3">
            <hr
                v-for="(img, i) in imgs"
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
    name: "CarouselView",
    props: {
        imgs: {
            type: Array,
            default: () => []
        },
    },
    data() {
        return {
            activeImage: 'https://bimba-aiueo.com/wp-content/uploads/2022/09/PRESTASI-biMBA-1600x666.jpg',
            transletX: 0,
            images: [
                'https://bimba-aiueo.com/wp-content/uploads/2022/09/PRESTASI-biMBA-1600x666.jpg',
                'https://bimba-aiueo.com/wp-content/uploads/2022/09/MURID-dan-UNIT.jpg',
                'https://bimba-aiueo.com/wp-content/uploads/2022/09/COBA-GRATIS-1600x666.jpg',
            ],
        }
    },
    mounted() {
        // this.setCarouselManualy()
    },
    methods: {
        setActiveImage(index) {
            this.transletX = (index / this.imgs.length) * 100
        },
        setCarouselManualy() {
            const length = this.imgs.length
            let index = 0
            for (index = 0; index < length; ) {
                setTimeout(() => {
                    this.transletX = (index / this.imgs.length) * 100
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
            const transletX = (index / this.imgs.length) * 100
            return transletX === this.transletX
        },
    },
}
</script>

<style></style>
