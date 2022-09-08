<script>
import KindWords from '../components/sections/home/KindWords.vue';
import Landing from '../components/sections/home/Landing.vue';
import LandingVeneers from '../components/sections/home/LandingVeneers.vue';
import Services from '../components/sections/home/Services.vue';
import OurClinic from '../components/sections/home/OurClinic.vue';
import ReachUs from '../components/sections/home/ReachUs.vue';

export default {
    components: { Landing, LandingVeneers, Services, KindWords, OurClinic, ReachUs }
}

</script>

<template>
    <section>
        <Landing />
        <LandingVeneers />
        <Services />
        <KindWords />
        <OurClinic />
        <ReachUs/>
    </section>
</template>