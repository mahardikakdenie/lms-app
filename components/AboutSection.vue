<template>
    <div class="">
        <div class="container">
            <div class="heading text-center">
                <h4 class="text-3xl font-bold font-cuss">Tentang Smile Learning Center</h4>
                <p class="text-lg font-cuss">Kami Memberikan Solusi terhadap buah hati anda</p>
            </div>
            <div class="grid gap-6 sm-grid-cols-2 lg:grid-cols-3">
               <base-list-section v-for="i in 3" :key="i" />
            </div>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&display=swap');
* {
    font-family: 'Delicious Handrawn', cursive;
}
</style>
