<template>
    <div class="">
        <div class="container">
            <div class="heading text-center">
                <h4 class="text-3xl font-bold font-cuss">Tentang Smile Learning Center</h4>
                <p class="text-lg font-cuss">Kami Memberikan Solusi terhadap buah hati anda</p>
            </div>
            <div data-aos="fade-right" class="grid gap-6 ml-[30px] sm-grid-cols-2 lg:grid-cols-3">
               <base-list-section v-for="i in 3" :key="i" />
            </div>
        </div>
    </div>
</template>

<script>
export default {}
</script>
