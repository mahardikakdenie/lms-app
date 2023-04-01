<template>
    <header id="navbar" class="lg:sticky sm:relative top-0 z-50 bg-black/10 transition duration-300 sticky-header bg-white lg:h-[100px] sm:h-[200px]">
        <div class="flex flex-col max-w-screen-xl mx-auto sm:items-start lg:items-center lg:justify-between lg:flex-row lg:h-[100px]">
            <div class="flex flex-col lg:flex-row lg:items-center sm:items-start space-x-4 xl:space-x-8">
                <div class="w-full flex flex-row lg:items-center sm:items-start justify-between py-6">
                    <div class="cursor-pointer flex" @click="$router.push('/')">
                        <img src="slc-dark.png" alt="" class="w-[233px]">
                    
                    </div>
                    <button class="rounded-lg lg:hidden focus:outline-none focus:shadow-outline" @click.prevent="openBurgerMenu">
                        <SegmentIcon v-if="!open" :size="24" />
                        <CloseIcon v-else :size="24" />
                    </button>
                </div>
            </div>
            <div :class="[open ? 'flex' : 'hidden lg:flex']" class="space-x-3">
                <ul
                    :class="[open ? 'flex' : 'hidden lg:flex']"
                    class="w-full h-auto flex flex-col flex-grow lg:items-center pb-4 lg:pb-0 lg:justify-end lg:flex-row origin-top duration-300 xl:space-x-2 space-y-3 lg:space-y-0"
                >
                    <NavLink v-for="(nav, i) in navs" :key="i" :name="nav.name" :url="nav.url" />
                    <li class="relative group">
                        <button
                            class="md:px-4 py-2 text-sm bg-transparent rounded-lg text-[#666666] hover:text-gray-900 focus:outline-none focus:shadow-outline flex items-center"
                            @click="dropdownToggler"
                            @blur="dropdownToggler"
                        >
                            <span>Lainnya</span>
                            <ChevronUpIcon v-if="dropdownNavbar" :size="16" />
                            <ChevronDownIcon v-else :size="16" />
                        </button>
                        <transition name="transform-fade-down">
                            <ul
                                v-if="dropdownNavbar"
                                class="flex lg:absolute flex-col max-w-42 py-1 lg:bg-white rounded-md lg:shadow-md pl-2 lg:pl-0"
                            >
                                <li>
                                    <a href="#" class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100"
                                        >Tentang</a
                                    >
                                </li>
                                <li>
                                    <a href="#" class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100"
                                        >Bimba Online</a
                                    >
                                </li>
                                <li>
                                    <a href="#" class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100"
                                        >Cari Kelas</a
                                    >
                                </li>
                                <li>
                                    <a href="#" class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100"
                                        >Kemitraan</a
                                    >
                                </li>
                                <li>
                                    <a href="#" class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100"
                                        >Relawan Pendidikan</a
                                    >
                                </li>
                                <li>
                                    <a href="#" class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100">Faq</a>
                                </li>
                                <li>
                                    <a href="#" class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100"
                                        >Lainnya</a
                                    >
                                </li>
                            </ul>
                        </transition>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>
<script>
export default {
    name: 'BaseNavbar',
    data() {
        return {
            open: false,
            dropdownNavbar: false,
            navs: [
                {
                    name: 'Tentang',
                    url: '/about-bimba'
                },
                // {
                //     name: 'Kelas Online',
                //     url: '/online-class',
                // },
                {
                    name: 'Cari Kelas',
                    url: '/search-class'
                },
                {
                    name: 'Relawan Pendidikan',
                    url: '/education-volunteer',
                },
                {
                    name: 'FAQ',
                    url: '/faq-slc',
                },
                {
                    name: 'Kontak',
                    url: '/contact-slc',
                },
            ],
        }
    },
    methods: {
        openBurgerMenu() {
            this.open = !this.open
        },
        dropdownToggler() {
            this.dropdownNavbar = !this.dropdownNavbar
        },
    },
}
</script>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@300&display=swap');
  .font-logo {
    font-family: 'Nunito', sans-serif !important;
  }
</style>