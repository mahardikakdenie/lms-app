<template>
    <div class="group rounded-3xl border-2 w-[308px] lg:w-[411px] border-white shadow-md p-6">
        <a
            v-tooltip.bottom-start="{ content: title, classes: 'bg-blue-200 p-2 font-bold rounded-md text-sm' }"
            href="services-detail.html"
            class="my-8 inline-block text-[19px] text-blue-700 font-bold dark:text-white dark:group-hover:text-black whitespace-nowrap font-cuss w-3/4 text-ellipsis overflow-hidden"
            >{{ title }}</a
        >
        <div class="h-[202px] flex items-center">
            <img :src="images" class="" style="background-size: 100% 100%" />
        </div>
        <div class="h-[60px]">
            <p
                v-tooltip.bottom-start="{
                    content: description,
                    classes: 'bg-blue-200 p-2 font-bold rounded-md text-sm',
                }"
                class="mb-10 mt-[30px] text-content-elipsis transition dark:group-hover:text-black text-md"
            >
                {{ description }}
            </p>
        </div>
        <button
            type="button"
            class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800 w-full font-bold"
        >
            Lihat Kelas
        </button>
    </div>
</template>

<script>
export default {
    props: {
        item: {
            type: Object,
            default: () => ({}),
        },
    },
    data() {
        return {
            desc: 'We provide services with the best designs than our designer team for your business',
            titlePage: 'Prestasi Smile Learning Center',
        }
    },
    computed: {
        images() {
            return (
                this.item?.img ??
                'https://images.unsplash.com/photo-1674574124792-3be232f1957f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80'
            )
        },
        description() {
            return this.item?.desc ?? this.desc
        },
        title() {
            return this.item?.title ?? this.titlePage
        },
    },
}
</script>

<style>
.text-content-elipsis {
    display: -webkit-box;
    max-width: 100%;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
}
</style>