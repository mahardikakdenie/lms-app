<template>
    <div class="">
        <div class="container">
            <div class="heading text-center">
                <h4 class="text-3xl font-bold font-cuss">Testimonial Orangtua</h4>
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
                    title: 'KATA BUNDA TENTANG BIMBA | BUNDA EKA BIMBA VILLA NUSA INDAH',
                    desc: 'Psikotropi Anak Lebih terpadu',
                    img: 'https://bimba-aiueo.com/wp-content/uploads/2020/05/testimoni-tumbnail-15.jpg',
                },
                {
                    title: 'KATA BUNDA TENTANG BIMBA | BUNDA EKA BIMBA VILLA NUSA INDAH',
                    desc: 'Psikotropi Anak Lebih terpadu',
                    img: 'https://bimba-aiueo.com/wp-content/uploads/2020/05/testimoni-tumbnail-15.jpg',
                },
                {
                    title: 'KATA BUNDA TENTANG BIMBA | BUNDA EKA BIMBA VILLA NUSA INDAH',
                    desc: 'Psikotropi Anak Lebih terpadu',
                    img: 'https://bimba-aiueo.com/wp-content/uploads/2020/05/testimoni-tumbnail-15.jpg',
                },
            ],
        }
    },
}
</script>