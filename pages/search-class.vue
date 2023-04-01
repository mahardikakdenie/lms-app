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
            <div class="flex justify-end">
                <div class="grid grid-rows-1 w-[25%]">
                    <input type="text" class="rounded py-1" placeholder="Cari Kelas">
                </div>
            </div>
            <div class="grid gap-6 ml-[30px] sm-grid-cols-2 lg:grid-cols-3">
                <base-list-class v-for="i in 3" :key="i" />
            </div>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style>
</style>