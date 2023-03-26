<template>
    <div>
        <div
            class="flex h-[720px] overflow-hidden transition duration-300 ease-in-out"
            :style="`width: ${images.length * 100}%; transform: translateX(-${transletX}%)`"
        >
            <div
                v-for="(image, i) in images"
                :key="i"
                class="bg-cover bg-gray-100 bg-black lg:bg-center bg-right w-full flex items-center bg-opacity-90"
                :style="`background-image: url(${image})`"
            >
                <div class="w-full flex flex-col container" data-v-3244602b="">
                    <div class="left flex items-center" data-v-3244602b="">
                        <div class="lg:w-1/2 text-black" style="color: #ffffff" data-v-3244602b="">
                            <h2 class="lg:text-4xl text-4xl xl:text-4xl font-bold leading-normal" data-v-3244602b="">
                                Lets Grow and Flow
                            </h2>
                            <div class="tracking-8% mt-5 lg:text-xl text-sm" data-v-3244602b="">
                                Brings you to the center of excellence of Indonesia's most prominent local-owned cloud
                                service
                            </div>
                        </div>
                    </div>
                    <div class="w-full mt-[47px] left" data-v-3244602b="">
                        <div class="flex flex-col md:flex-row md:gap-34px gap-3 w-full md:w-auto" data-v-3244602b="">
                            <a
                                href="https://bss.floucloud.id/login"
                                class="btn-hover-translate bg-white py-2.5 px-4 text-sm rounded-lg font-medium w-full md:w-auto text-center"
                                style="background-color: #004d7d; color: #ffffff"
                                data-v-3244602b=""
                            >
                                Get Started </a
                            ><a
                                href="https://floucloud.id/contact-us/"
                                class="btn-hover-translate bg-white py-2.5 px-4 text-sm rounded-lg font-medium w-full md:w-auto text-center"
                                style="background-color: #f1f1f2; color: #004d7d"
                                data-v-3244602b=""
                            >
                                Contact Us
                            </a>
                        </div>
                    </div>
                </div>
            </div>
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
                'https://apicms1.floucloud.id:4443/uploads/carousel/1d2d613c-1c1d-47ef-b4bf-a40157e83302.jpg'
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
            let index = 0
            for (index = 0; index < length; ) {
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
