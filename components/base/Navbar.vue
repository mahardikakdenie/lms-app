<template>
    <nav id="navbar" class="relative z-10 w-full text-neutral-800">
        <div class="flex flex-col max-w-screen-xl px-8 mx-auto lg:items-center lg:justify-between lg:flex-row py-4">
            <div class="flex flex-col lg:flex-row items-center space-x-4 xl:space-x-8">
                <div class="w-full flex flex-row items-center justify-between py-6">
                    <div class="cursor-pointer" @click="$router.push('/')">
                        <img
                            src="https://bimba-aiueo.com/wp-content/uploads/2015/08/logobimbaaiueo-small.jpg"
                            class="w-24 xl:w-56 cursor-pointer"
                            alt="Nefa Logo"
                        />
                    </div>
                    <button class="rounded-lg lg:hidden focus:outline-none focus:shadow-outline" @click="open = !open">
                        <SegmentIcon v-if="!open" :size="24" />
                        <CloseIcon v-else :size="24" />
                    </button>
                </div>
            </div>
            <div :class="[open ? 'flex' : 'hidden lg:flex']" class="space-x-3">
                <!-- <base-button class="px-8 xl:px-10 py-3 mt-2 bg-inherit text-gradient border border-[#0c66ee]">
		Login
		</base-button>
		<base-button class="px-8 xl:px-10 py-3 mt-2 bg-gradient-to-r from-[#468ef9] to-[#0c66ee] text-white">
		Sign Up
		</base-button> -->
                <ul
                    :class="[open ? 'flex' : 'hidden lg:flex']"
                    class="w-full h-auto flex flex-col flex-grow lg:items-center pb-4 lg:pb-0 lg:justify-end lg:flex-row origin-top duration-300 xl:space-x-2 space-y-3 lg:space-y-0"
                >
                    <NavLink name="Tentang" url="/about-bimba" />
                    <NavLink name="Bimba Online" url="#" />
                    <NavLink name="Cari Kelas" url="#" />
                    <NavLink name="Kemitraan" url="#" />
                    <NavLink name="Relawan Pendidikan" url="#" />
                    <NavLink name="Faq" url="#" />
                    <NavLink name="Kontak" url="#" />
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
    </nav>
</template>
<script>
export default {
    name: 'BaseNavbar',
    data() {
        return {
            open: false,
            dropdownNavbar: false,
        }
    },
    methods: {
        dropdownToggler() {
            this.dropdownNavbar = !this.dropdownNavbar
        },
    },
}
</script>
