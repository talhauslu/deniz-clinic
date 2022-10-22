<script>
import Dropdown from '../components/Dropdown/Dropdown.vue';
import Element from '../components/Dropdown/Element.vue';
import Subelement from '../components/Dropdown/Subelement.vue';
export default {
    props: {
        navbarOpen: Boolean
    },
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
        });
    },
    mounted() {
        window.addEventListener("scroll", this.handleScroll);
    },
    destroyed() {
        window.removeEventListener("scroll", this.handleScroll);
    },
    methods: {
        handleScroll(event) {
            if (window.scrollY > 128) {
                this.top = "hidden";
            }
            else if (window.scrollY < 64) {
                this.top = "flex";
            }
        },
        toggleNavbar() {
            this.$emit("togglenavbar");
        }
    },
    components: { Dropdown, Element, Subelement }
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
                        <span class="font-semibold">Pazartesi - Cuma</span>
                        <span>09:00 - 17:00</span>
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
                    <a target="_blank" href="https://www.instagram.com/dr.denizyilmaz"><i
                            class="fa-brands fa-instagram cursor-pointer p-2 rounded-full hover:bg-gray-200"></i></a>
                    <i class="fa-brands fa-linkedin cursor-pointer p-2 rounded-full hover:bg-gray-200"></i>
                    <a target="_blank" href="https://wa.me/+905306509433"><i
                            class="fa-brands fa-whatsapp cursor-pointer p-2 rounded-full hover:bg-gray-200"></i></a>
                </div>
            </div>
            <div id="sticky"
                class="flex flex-row md:flex-col lg:flex-row gap-4 1120:gap-0 w-full justify-between px-6 py-2 bg-opacity-60 items-center h-auto bg-indigo-50 sticky top-0">

                <NuxtLink to="/" class="h-auto w-2/3 400:w-auto 400:h-20">
                    <img src="/logo-removebg-preview.png" class="object-contain h-full w-full" />
                </NuxtLink>

                <div class="hidden md:flex flex-col 1120:flex-row w-full 1120:w-auto justify-around items-center gap-8">
                    <nav class="flex flex-row gap-8 font-bold text-gray-600 text-sm flex-wrap">
                        <NuxtLink to="/">ANA SAYFA</NuxtLink>

                        <Dropdown title="SERVİSLER">
                            <!-- <Element to="/esthetic-cosmetic" title="Estetik&Kozmetik Diş Hekimliği" /> -->
                            <Element to="/esthetic-cosmetic" title="Estetik & Kozmetik Diş Hekimliği" />
                            <Element to="/smile-design" title="Gülüş Tasarımı" />
                            <Element to="/porcelain-laminate" title="Porselen Lamina" />
                            <Element to="/tooth-whitening" title="Diş Beyazlatma" />
                            <!-- <Element to="/esthetic-cosmetic/porselen-inlay-onlay" title="Porselen & Inlay Onlay" />
                            <Element to="/esthetic-cosmetic/dis-eti-estetigi" title="Diş Eti Estetiği" />
                            
                            <Element to="/esthetic-cosmetic/zirkonyum-porselen" title="Zirkonyum Porselen Kaplama" /> -->
                        </Dropdown>

                        <NuxtLink to="/about">HAKKIMIZDA</NuxtLink>
                        <NuxtLink to="/blog">BLOG</NuxtLink>
                        <NuxtLink to="/media">MEDYA</NuxtLink>
                        <NuxtLink to="/contact">İLETİŞİM</NuxtLink>
                    </nav>

                    <button
                        class="hidden 1120:flex p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all">
                        Randevu Al
                    </button>
                </div>
                <transition name="mobileNavButton">
                    <i v-if="!navbarOpen" @click="toggleNavbar" class="fa-solid fa-bars block md:hidden text-3xl"></i>
                    <i v-else @click="toggleNavbar" class="fa-solid fa-x block md:hidden text-3xl"></i>
                </transition>
            </div>
        </div>

    </header>
</template>

<style>
.mobileNavButton-enter-active,
.mobileNavButton-leave-active {
    transition: all 0.25s ease-out;
}

.mobileNavButton-enter-from {
    opacity: 0;
    transform: translateY(30px);
}

.mobileNavButton-leave-to {
    opacity: 0;
    transform: translateY(-30px);
}
</style>