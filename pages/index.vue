<script>
import KindWords from '../components/sections/home/KindWords.vue';
import Landing from '../components/sections/home/Landing.vue';
import LandingVeneers from '../components/sections/home/LandingVeneers.vue';
import Services from '../components/sections/home/Services.vue';


    export default{
    components: { Landing, LandingVeneers, Services, KindWords }
}

</script>

<template>
    <section>
        <Landing />
        <LandingVeneers />
        <Services/>
        <KindWords/>
    </section>
</template>