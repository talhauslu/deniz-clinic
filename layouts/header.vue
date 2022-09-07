<script>
export default {
    data() {
        return ({
            top: "flex",
            services: [
                { name: "Hizmet 1", url: "/" },
                { name: "Hizmet 2", url: "/" },
                { name: "Hizmet 3", url: "/" },
                { name: "Hizmet 4", url: "/" },
                { name: "Hizmet 5", url: "/" },

            ]
        })
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    destroyed() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll(event) {
            if (window.scrollY > 128) {
                this.top = "hidden"
            }
            else if (window.scrollY < 64) {
                this.top = "flex"
            }
        }
    },
}
</script>

<template>
    <header class="z-50 shadow sticky top-0">
        <div class="relative w-full bg-white ">
            <div :class="`hidden md:${top} md:flex-row w-full h-16 justify-around text-gray-600 p-3 `">
                <div class="flex flex-row justify-around items-center gap-2">
                    <i class="fa-solid fa-location-dot text-4xl text-pink-200"></i>
                    <div class="text-sm flex flex-col flex-around">
                        <span class="font-semibold">Akmerkez Residence Daire:7B1</span>
                        <span>Beşiktaş/İstanbul</span>
                    </div>
                </div>
                <div class="flex flex-row justify-around items-center gap-2">
                    <i class="fa-solid fa-clock text-4xl text-pink-200"></i>
                    <div class="text-sm flex flex-col flex-around">
                        <span class="font-semibold">Monday - Friday</span>
                        <span>9 AM - 5 PM</span>
                    </div>
                </div>
                <div class="flex flex-row justify-around items-center gap-2">
                    <i class="fa-solid fa-mobile-screen text-4xl text-pink-200"></i>
                    <div class="text-sm flex flex-col flex-around">
                        <span class="font-semibold">+90 530 650 94 33</span>
                        <span>denizyilmaz@xyz.com</span>
                    </div>
                </div>
                <div class="flex flex-row justify-around items-center gap-4 text-2xl text-gray-600 ">
                    <i class="fa-brands fa-instagram cursor-pointer p-2 rounded-full hover:bg-gray-200"></i>
                    <i class="fa-brands fa-linkedin cursor-pointer p-2 rounded-full hover:bg-gray-200"></i>
                    <i class="fa-brands fa-whatsapp cursor-pointer p-2 rounded-full hover:bg-gray-200"></i>
                </div>
            </div>
            <div id="sticky"
                class="flex flex-row md:flex-col lg:flex-row gap-4 1120:gap-0 w-full justify-between px-6 py-2 bg-opacity-60 items-center h-auto bg-indigo-50 sticky top-0">

                <img src="/logo-removebg-preview.png" class="object-contain h-auto w-2/3 400:w-auto 400:h-20" />

                <div class="hidden md:flex flex-col 1120:flex-row w-full 1120:w-auto justify-around items-center gap-8">
                    <nav class="flex flex-row gap-8 font-bold uppercase text-gray-600 text-sm flex-wrap">
                        <NuxtLink to="/home">ANA SAYFA</NuxtLink>

                        <div class="relative group cursor-pointer">
                            <div class=" relative flex flex-row align-center justify-center gap-2">
                                <span>HİZMETLERİMİZ</span>
                                <i class="fa-solid fa-sort-down"></i>
                            </div>
                            <div
                                class="flex absolute invisible opacity-0 bg-white group-hover:visible group-hover:opacity-100 transition duration-400 w-80 flex-col align-center shadow-lg left-0 right-0">
                                <span v-for="service of services"
                                    class="p-4 hover:bg-pink-100 cursor-pointer">{{service.name}}</span>
                            </div>
                        </div>

                        <NuxtLink to="/home">HAKKIMIZDA</NuxtLink>
                        <NuxtLink to="/home">BLOG</NuxtLink>
                        <NuxtLink to="/home">MEDYA</NuxtLink>
                        <NuxtLink to="/home">İLETİŞİM</NuxtLink>
                    </nav>

                    <button
                        class="hidden 1120:flex p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all">
                        Randevu Al
                    </button>
                </div>
                <i class="fa-solid fa-bars block md:hidden text-3xl"></i>
            </div>
        </div>

    </header>
</template>

<style>
</style>