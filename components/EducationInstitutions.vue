<template>
    <div class="mt-[68px]">
        <div class="container">
            <div class="heading text-center">
                <h4 class="text-3xl font-bold font-cuss">Education institutions</h4>
                <p class="text-lg font-cuss">Kami Memberikan Solusi terhadap buah hati anda</p>
            </div>
            <div class="grid gap-6 ml-[30px] sm-grid-cols-2 lg:grid-cols-3">
                <base-list-section v-for="(item, i) in testimonials" :key="i" :item="item" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
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