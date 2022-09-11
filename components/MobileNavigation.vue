<script>
export default {
    props: {
        open: {
            type: Boolean,
            default: false,
            required: true
        }
    },
    methods:{
        toggleSubmenu(){
            this.submenuOpen = !this.submenuOpen
        }
    },
    data() {
        return ({
            submenuOpen: false,
            services: [
                { name: "Hizmet 1", url: "/" },
                { name: "Hizmet 2", url: "/" },
                { name: "Hizmet 3", url: "/" },
                { name: "Hizmet 4", url: "/" },
                { name: "Hizmet 5", url: "/" },
            ]
        })
    }
}
</script>

<template>
    <transition name="mobileNav">
    <div v-if="open" class="w-screen min-h-screen overflow-y-auto fixed z-50 right-0 flex flex-col items-center bg-white p-4 px-8 gap-4">
        <nuxt-img src="/logo2-removebg-preview.png" class="h-1/6 object-contain" />

        <div class="flex flex-col gap-4 w-full ">
            <div class="self-center">
                <label>Language: </label>
                <select class="inline">
                    <option>Türkçe</option>
                    <option>English</option>
                    <option>Deutsch</option>
                </select>
            </div>
            <nav class="flex flex-col font-bold uppercase text-gray-600">
                <NuxtLink class="border-b p-2" to="/">ANA SAYFA</NuxtLink>

                <div class="border-b p-2">
                    <div class="flex flex-row items-center" @click="toggleSubmenu">
                        <span class="inline">HİZMETLERİMİZ </span>
                        <i class="fa-solid fa-sort-down inline"></i>
                    </div>
                    <transition name="submenu">
                        <div v-if="submenuOpen"
                            class="flex flex-col">
                            <span v-for="service of services"
                                class="hover:bg-pink-100 cursor-pointer p-2 border-b pl-1">{{service.name}}</span>
                        </div>
                    </transition>
                </div>

                <NuxtLink class="border-b p-2" to="/about">HAKKIMIZDA</NuxtLink>
                <NuxtLink class="border-b p-2" to="/blog">BLOG</NuxtLink>
                <NuxtLink class="border-b p-2" to="/media">MEDYA</NuxtLink>
                <NuxtLink class="border-b p-2" to="/contact">İLETİŞİM</NuxtLink>
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
    height: 0;
    opacity: 0
}

.submenu-enter-active,
.submenu-leave-active {
    transition: 0.5s;
}

.submenu-enter-to,
.submenu-leave-from {
    height: auto;
    opacity: 1
}
</style>