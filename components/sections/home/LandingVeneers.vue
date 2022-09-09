<script>
export default {
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
    <div class="flex flex-col bg-blue-50 ">
        <div aos-data="fade-up" class="w-full bg-blue-100  text-center py-8">
            <div class="w-full text-white bg-blue-300 shadow-md p-8">
                <h1 class="text-lg">Uzm. Dr. Deniz Yılmaz Diş Kliniği</h1>
                <h2 class="text-sm">Kültür mahallesi Ahmet Adnan Saygun Caddesi No:3 Akmerkez Residence Daire:7B1, 34337
                    Beşiktaş/İstanbul</h2>
            </div>
        </div>
        <div class="w-full flex flex-col items-center justify-around md:flex-row p-4 md:p-14">
            <nuxt-img aos-data="fade-right" class="object-contain w-2/3 md:w-5/12 rounded-xl shadow-lg" src="/veneers.png" />
            <div aos-data="fade-left" class="w-full md:w-1/2 flex flex-col gap-10 justify-around p-2 py-8 sm:p-8 md:p-4 ">
                <h1 class="text-6xl">Dental Veneers</h1>
                <h2 class="text-4xl text-gray-800">Daha
                    <span class="text-blue-400">{{ current }}|</span>
                </h2>
                <span>Veneers hakkında teknik olmayan kısa bir açıklama. Lorem ipsum dolor sit amet consectetur
                    adipisicing elit. Accusamus quos asperiores nemo dolore. Saepe iure sit minus optio omnis nihil quas
                    ipsam, repellendus laudantium quod. Veritatis dolorem officiis neque nihil!</span>
                <button
                    class="inline self-start p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all shadow-md">
                    Daha fazlası
                </button>
            </div>
        </div>
    </div>



</template>