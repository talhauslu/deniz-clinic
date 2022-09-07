<script>
import Landing from '../components/sections/home/Landing.vue';
import LandingVeneers from '../components/sections/home/LandingVeneers.vue';
import Services from '../components/sections/home/Services.vue';

    export default{
    components: { Landing, LandingVeneers, Services }
}

</script>

<template>
    <section>
        <Landing />
        <LandingVeneers />
        <Services/>
    </section>
</template>