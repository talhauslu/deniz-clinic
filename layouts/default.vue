<script>

import Header from './header.vue';
import Footer from './footer.vue';
export default {
    components: { Header, Footer }
}

</script>

<template>
    <main class="overflow-x-hidden">
        <Header />
        <Nuxt />
        <Footer />
        <nuxt-img class="fixed bottom-0 right-0 w-14 h-14 mr-4 mb-4 cursor-pointer z-50" src="/whatsapp.png"/>
    </main>
</template>