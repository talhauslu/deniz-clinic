<script>
import Landing from '../components/Landing.vue';
import LandingVeneers from '../components/LandingVeneers.vue';
import Services from '../components/Services.vue';

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