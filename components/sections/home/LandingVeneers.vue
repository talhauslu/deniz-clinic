<script>
import TypeWriter from './../../TypeWriter.vue'
export default {
    components:{
        TypeWriter
    },
    data() {
        return ({
            words: ["beyaz", "doğal"],
            current: ""
        })
    },
    methods: {
        async type(word) {
            // console.log("type worked", this.current)
            for (var letter of word) {
                await new Promise(r => setTimeout(r, 150));
                this.current = this.current + letter
            }
            await new Promise(r => setTimeout(r, 1000));
        },
        async delete() {
            for (var letter of this.current) {
                await new Promise(r => setTimeout(r, 150));
                this.current = this.current.slice(0, -1)
            }
            await new Promise(r => setTimeout(r, 1000));
        }
    },
    async created() {
        while (true) {
            for (var word of this.words) {
                await this.type(word)
                await this.delete()
            }
        }
    }
}
</script>

<template>

    <section class="animation-element w-full flex flex-col items-center justify-around md:flex-row bg-shift-wb text-white md:h-90vh gap-4 md:gap-0 p-8 md:p-0 relative">
        <nuxt-img class="animation-element fade-left object-cover w-4/5 md:w-1/2 shadow-lg" src="/veneers.png" />
        <div class="animation-element fade-right w-full md:w-1/2 flex flex-col gap-4 md:gap-12 justify-around md:p-8">
            <h1 class="text-6xl">Porselen Lamina</h1>
            <h2 class="text-4xl flex flex-col sm:flex-row gap-1 text-gray-400">
                <span>Daha</span> <span> </span>
                <TypeWriter class="text-blue-100" :speed="100" :delay="500"
                    :words="['beyaz','doğal']" />
            </h2>
            <span>Veneers hakkında teknik olmayan kısa bir açıklama. Lorem ipsum dolor sit amet consectetur
                adipisicing elit. Accusamus quos asperiores nemo dolore. Saepe iure sit minus optio omnis nihil quas
                ipsam, repellendus laudantium quod. Veritatis dolorem officiis neque nihil!</span>
            <NuxtLink to="/porcelain-laminate"
                class="inline self-start p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all  shadow-md">
                Daha fazlası
            </NuxtLink>
        </div>
        <nuxt-img class="hidden md:block absolute right-0 top-0" src="/dots-corner.png"></nuxt-img>
    </section>

</template>