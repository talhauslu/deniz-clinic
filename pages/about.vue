<script>
import Description from '../components/sections/about/Description.vue';
import ReachUs from '../components/ReachUs.vue';
import { onMounted, onUnmounted } from 'vue'
import Animatable from '../components/animation/animatable.vue';
import Landing from '../components/sections/about/Landing.vue';
import TeamMember from '../components/sections/about/TeamMember.vue';
export default {
    components: {
    Description,
    ReachUs,
    Animatable,
    Landing,
    TeamMember
}
}
</script>

<template>
    <Animatable>
        <Landing/>
        <Description />
        <h1 class="p-4 text-4xl font-semibold text-center bg-white">Ekibimiz</h1>
        <TeamMember/>
        <TeamMember/>
        <TeamMember/>
        <TeamMember/>
        <ReachUs />
        <!-- LAND -->
    </Animatable>
</template>