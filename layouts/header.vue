<script>
import Dropdown from '../components/Dropdown/Dropdown.vue';
import Element from '../components/Dropdown/Element.vue';
import Subelement from '../components/Dropdown/Subelement.vue';
export default {
    props: {
        navbarOpen: { type: Boolean },
    },
    data() {
        return ({
            top: "flex",
            services: [
                { name: "Estetik & Kozmetik Diş Hekimliği", url: "/esthetic-cosmetic" },
                { name: "Gülüş Tasarımı", url: "/smile-design" },
                { name: "Porselen Lamina", url: "/porcelain-laminate" },
                { name: "Diş Beyazlatma", url: "/tooth-whitening" },
                { name: "Zirkonyum Porselen Kaplama", url: "/zirconium-crowns" },
                { name: "İnlay & Onlay", url: "/inlay-onlay" },
                { name: "Diş Eti Estetiği", url: "/gum-esthetic" },
            ],
            languages: [
                { code: "tr", name: "Türkçe" },
                { code: "en", name: "English" }
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
    <header
        class="z-50 h-10vh shadow sticky top-0 flex flex-row sm:gap-4 md:gap-8 w-full justify-between sm:justify-center px-6 py-2 items-center bg-white font-semibold text-gray-700 text-lg ">

        <nav class="hidden sm:flex flex-row sm:gap-4 md:gap-8 flex-1 justify-end">
            <NuxtLink :to="localePath($t('header').navigation.routes.main.url)">{{$t('header').navigation.routes.main.name}}</NuxtLink>

            <Dropdown :title="$t('header').navigation.routes.services.name">

                <Element v-for="service in $t('header').navigation.services" :to="localePath(service.url)" :title="service.name" :key="service.url" />

            </Dropdown>
            <NuxtLink :to="localePath($t('header').navigation.routes.about.url)">{{$t('header').navigation.routes.about.name}}</NuxtLink>
        </nav>

        <NuxtLink :to="localePath($t('header').navigation.routes.main.url)" class="h-full py-1 block sm:hidden lg:block">
            <nuxt-img src="/logo-removebg-preview.png" class="object-contain h-full w-full" />
        </NuxtLink>

        <nav class="flex-1 hidden sm:flex flex-row sm:gap-4 md:gap-8 justify-start">

            <NuxtLink :to="localePath($t('header').navigation.routes.blog.url)">{{$t('header').navigation.routes.blog.name}}</NuxtLink>
            <NuxtLink :to="localePath($t('header').navigation.routes.before_after.url)">{{$t('header').navigation.routes.before_after.name}}</NuxtLink>
            <NuxtLink :to="localePath($t('header').navigation.routes.contact.url)">{{$t('header').navigation.routes.contact.name}}</NuxtLink>
            <!-- <select>
                <option value="tr">Turkish</option>
            </select> -->
            <div class="group absolute float-right right-8 flex flex-col items-center gap-4">
                <i class="fa-solid fa-globe hidden sm:flex text-xl cursor-pointer" name="language-popup"></i>
                <div class="absolute hidden group-hover:flex flex-col bg-white text-black items-center top-7 text-lg border shadow rounded-sm">

                    <span :class="{ 'bg-yellow-300': language.code === $i18n.locale }"
                        class="p-0.5 w-full hover:bg-yellow-200 cursor-pointer select-none"
                        v-for="language in $i18n.locales" :key="language.name">
                        <NuxtLink :to="switchLocalePath(language.code)">{{ language.name }}</NuxtLink>
                    </span>

                </div>
            </div>
        </nav>





        <transition name="mobileNavButton">
            <i v-if="!navbarOpen" @click="toggleNavbar" class="fa-solid fa-bars block sm:hidden text-3xl"></i>
            <i v-else @click="toggleNavbar" class="fa-solid fa-x block sm:hidden text-3xl"></i>
        </transition>

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
