<template>
    <div>
        <div class="bg-cover bg-gray-100 lg:bg-center w-full p-[67px] pb-[94px]">
            <div class="w-full flex flex-col container">
                <div class="left">
                    <div class=".lg:w-1/2.text-black text-center">
                        <span class="text-2xl font-bold leading-normal"> Cari Kelas Smile Learning Center </span>
                        <div class="tracking-8% mt-5 text-black lg:text-xl text-sm" data-v-3244602b="">
                            Providing reliable, flexible and premium quality cloud computing services. Flou understands
                            that efficiency, security, and a friendly approach are what you're looking for.
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="container py-[40px]">
            <div v-if="false" class="flex justify-end">
                <div class="grid grid-rows-1 w-[25%]">
                    <!-- <span class="icon material-icons">search</span>   -->
                    <input type="text" class="rounded py-1" placeholder="Cari Kelas">
                </div>
            </div>
            <div class="grid gap-6 ml-[30px] sm-grid-cols-2 lg:grid-cols-3">
                <base-list-class v-for="(item, i) in testimonials" :key="i" :item="item" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "SearchClass",
    data() {
        return {
            testimonials: [
                {
                    title: 'Bimba AIUEO',
                    desc: 'biMBA adalah proses bimbingan Minat Belajar Anak yang bertujuan agar anak minat, senang, suka dan gemar belajar sehingga terbangun pondasi karakter pembelajar yang kuat',
                    img: 'https://bimba-aiueo.com/wp-content/uploads/2015/08/logobimbaaiueo-small.jpg',
                },
                {
                    title: 'SEMPOA SIP',
                    desc: 'Tempat belajar sempoa yang beda, dapat diikuti melalui offline atau online bersama pengajar terbaik untuk memaksimalkan potensi kecerdasan Anak Anda',
                    img: 'https://www.sempoasip.com/Guest/img/location-home.png',
                },
                {
                    title: 'ENGLISH bIMBA',
                    desc: 'English biMBA Talk Programs (Distance Learning Center)',
                    img: 'https://www.english.bimba-aiueo.com/wp-content/uploads/2022/09/Logo-EbT-Fix-2@2x.png',
                },
            ],
        }
    },
}
</script>

<style>
</style>