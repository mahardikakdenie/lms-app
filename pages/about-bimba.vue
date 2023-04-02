<template>
    <div class="container">
        <!--  -->
        <div class="">
            <nav class="flex" aria-label="Breadcrumb">
                <ol class="inline-flex items-center space-x-1 md:space-x-3">
                    <li class="inline-flex items-center">
                        <a
                            href="#"
                            class="inline-flex items-center text-sm font-medium text-gray-700 hover:text-blue-600 dark:text-gray-400 dark:hover:text-white"
                        >
                            <svg
                                aria-hidden="true"
                                class="w-4 h-4 mr-2"
                                fill="currentColor"
                                viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
                                ></path>
                            </svg>
                            Home
                        </a>
                    </li>
                    <li>
                        <div class="flex items-center">
                            <svg
                                aria-hidden="true"
                                class="w-6 h-6 text-gray-400"
                                fill="currentColor"
                                viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                                    clip-rule="evenodd"
                                ></path>
                            </svg>
                            <a
                                href="#"
                                class="ml-1 text-sm font-medium text-gray-700 hover:text-blue-600 md:ml-2 dark:text-gray-400 dark:hover:text-white"
                                >About</a
                            >
                        </div>
                    </li>
                </ol>
            </nav>
        </div>

        <!--  -->
        <div class="mt-[30px]">
            <h2 class="text-2xl">Tentang Smile Learning Center</h2>
            <p class="mt-2">Recently updated on Desember 14th, 2020 at 08:37 am</p>
        </div>
        <div class="mt-6">
            <img
                class="w-full rounded shadow-md"
                src="https://bimba-aiueo.com/wp-content/uploads/2016/12/slide-bimba3.jpg"
                alt=""
            />
        </div>
        <div class="mt-6 py-6">
            <div class="mt-2 text-2xl my-2 font-bold">Apa itu Smile Learning Center</div>
            <p class="text-md">
                Sesuai dengan cara penulisan bi ditulis dengan huruf kecil dan MBA ditulis dengan huruf besar, biMBA
                adalah proses bimbingan Minat Belajar Anak yang bertujuan agar anak minat, senang, suka, dan gemar
                belajar sehingga terbangun pondasi karakter pembelajar yang kuat dalam rangka terwujudnya generasi
                pembelajar mandiri sepanjang hayat. Pembelajar adalah orang yang suka belajar, orang yang menghubungkan
                suatu dengan suatu lainnya untuk perbaikan diri dan lingkungannya.
            </p>
            <br />
            <p class="text-md">
                Salah satu bagian dari biMBA, biMBA AIUEO adalah proses bimbingan Minat Baca Anak yang bertujuan agar
                anak Minat, senang, suka, dan gemar membaca sehingga terbangun pondasi karakter gemar membaca. Kegiatan
                membaca merupakan bagian terpenting dalam kegiatan belajar.
            </p>
        </div>
        <div>
            <ul class="py-2">
                <AboutAccordion v-for="(accordion, index) in accordions" :key="index" :accordion="accordion" />
            </ul>
        </div>
        <div class="w-full flex justify-center">
            <a
                v-smooth-scroll
                data-aos="flip-down"
                data-aos-delay="150"
                href="#navbar"
                class="px-6 py-3 flex items-center space-x-2 bg-[#FAFAFA] hover:bg-gray-100 hover:shadow-md border border-[#DDDDDD] rounded-md text-gray-700"
            >
                <span>Back to top</span>
                <ArrowUpIcon :size="20" />
            </a>
        </div>
    </div>
</template>

<script>
import aosMixin from '@/mixins/aos'
export default {
    mixins: [aosMixin],
    data() {
        return {
            imgs: ['https://bimba-aiueo.com/wp-content/uploads/2016/12/slide-bimba3.jpg'],
            accordions: [
                {
                    title: 'Tujuan Bimba',
                    description:
                        "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over 8 million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
                },
                {
                    title: 'How secure is NEFA?',
                    description:
                        "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
                },
                {
                    title: 'Do I have to buy a whole Bitcoin?',
                    description:
                        "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
                },
                {
                    title: 'How do I actually buy Bitcoin?',
                    description:
                        "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
                },
            ],
        }
    },
}
</script>

<style></style>
