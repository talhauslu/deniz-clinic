<script>
import Description from '../components/sections/about/Description.vue';
import ReachUsForm from '../components/ReachUsForm.vue';
import { onMounted, onUnmounted } from 'vue'
import Animatable from '../components/animation/animatable.vue';
import Landing from '../components/sections/about/Landing.vue';
import TeamMember from '../components/sections/about/TeamMember.vue';
export default {
    components: {
    Description,
    ReachUsForm,
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
        <!-- <ReachUsForm class="w-1/2"/> -->
        <!-- LAND -->
    </Animatable>
</template>