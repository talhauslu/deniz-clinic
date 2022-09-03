<script>

import Header from './header.vue';
import Footer from './footer.vue';
export default {
    components: { Header, Footer }
}

</script>

<template>
    <main>
        <Header />
            <Nuxt />
        <Footer/>
    </main>
</template>