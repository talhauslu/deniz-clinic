<script>
export default {
    props: {
        open: {
            type: Boolean,
            default: false,
            required: true
        }
    },
    methods: {
        toggleSubmenu() {
            this.submenuOpen = !this.submenuOpen
        },
        toggleNavbar() {
            this.$emit("togglenavbar")
        }
    },
    data() {
        return ({
            submenuOpen: false,
            services: [
                { name: "Estetik & Kozmetik Diş Hekimliği", url: "/esthetic-cosmetic" },
                { name: "Gülüş Tasarımı", url: "/smile-design" },
                { name: "Porselen Lamina", url: "/porcelain-laminate" },
                { name: "Diş Beyazlatma", url: "/tooth-whitening" },
                { name: "Zirkonyum Porselen Kaplama", url: "/zirconium-crowns" },
                { name: "İnlay & Onlay", url: "/inlay-onlay" },
                { name: "Diş Eti Estetiği", url: "/gum-esthetic" },
            ]
        })
    }
}
</script>

<template>
    <transition name="mobileNav">
        <div v-if="open" class="w-screen h-screen overflow-y-auto fixed z-50 top-0 bottom-0 bg-white right-0 ">

            <div class="w-full h-full relative flex flex-col justify-evenly p-4 px-8 gap-4 text-lg">

                <i @click="toggleNavbar" class="fa-solid fa-x block text-3xl absolute right-4 top-4"></i>

                <nuxt-img src="/logo-removebg-preview.png" class="w-11/12 object-contain self-center" />

                <div class="self-center">
                    <label>Language: </label>
                    <select class="inline">
                        <option>Türkçe</option>
                        <option>English</option>
                        <option>Deutsch</option>
                    </select>
                </div>


                <nav class="flex flex-col font-bold text-gray-600">
                    <NuxtLink @click.native="toggleNavbar" class="border-b p-2" to="/">ANA SAYFA</NuxtLink>

                    <div class="border-b p-2">
                        <span @click="toggleSubmenu"
                            class="inline-flex flex-row items-center"><span>HİZMETLERİMİZ</span> <i
                                class="fa-solid fa-sort-down inline"></i></span>
                        <transition name="submenu">
                            <div v-if="submenuOpen" class="flex flex-col">
                                <NuxtLink @click.native="toggleNavbar" v-for="service of services" :to="service.url"
                                    :key="service.url" class="hover:bg-pink-100 cursor-pointer p-2 pl-1">•
                                    {{ service.name }}</NuxtLink>
                            </div>
                        </transition>
                    </div>

                    <NuxtLink @click.native="toggleNavbar" class="border-b p-2" to="/about">HAKKIMIZDA</NuxtLink>
                    <NuxtLink @click.native="toggleNavbar" class="border-b p-2" to="/blog">BLOG</NuxtLink>
                    <NuxtLink @click.native="toggleNavbar" class="border-b p-2" to="/media">MEDYA</NuxtLink>
                    <NuxtLink @click.native="toggleNavbar" class="border-b p-2" to="/contact">İLETİŞİM</NuxtLink>
                </nav>
            </div>

        </div>
    </transition>
</template>

<style scoped>
.mobileNav-enter,
.mobileNav-leave-to {
    width: 0;
    opacity: 0
}

.mobileNav-enter-active,
.mobileNav-leave-active {
    transition: 0.6s;
}

.mobileNav-enter-to,
.mobileNav-leave-from {
    width: 100%;
    opacity: 1
}

.submenu-enter,
.submenu-leave-to {
    transform: scaleY(0);
    opacity: 0
}

.submenu-enter-active,
.submenu-leave-active {
    transition: 0.5s;
}

.submenu-enter-to,
.submenu-leave-from {
    transform: scaleY(1);
    opacity: 1
}
</style>