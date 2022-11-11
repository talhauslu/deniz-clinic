<script>
import Header from './header.vue';
import Footer from './footer.vue';
import MobileNavigation from '../components/MobileNavigation.vue';
export default {
    components: { Header, Footer, MobileNavigation },
    data(){
        return({
            navbarOpen:false
        })
    },
    methods:{
        toggleNavbar(){
            this.navbarOpen = !this.navbarOpen
        }
    }
}

</script>

<template>
    <main class="bg-white">
        <Header :navbarOpen="navbarOpen"  @togglenavbar="toggleNavbar"/>
        <MobileNavigation @togglenavbar="toggleNavbar" :open="navbarOpen"/>
        <Nuxt />
        <Footer />
        <a target="_blank" class="fixed bottom-0 right-0 w-14 h-14 mr-4 mb-4 cursor-pointer z-50" href="https://wa.me/+905306509433"><nuxt-img class="w-full h-full" src="/whatsapp.png" /></a>
    </main>
</template>