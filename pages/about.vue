<script>
import Landing from '../components/sections/about/Landing.vue';
import ReachUsForm from '../components/ReachUsForm.vue';
import { onMounted, onUnmounted } from 'vue'
import Animatable from '../components/animation/animatable.vue';
export default {
    components: {
    Landing,
    ReachUsForm,
    Animatable
}
}
</script>

<template>
    <Animatable>
        <Landing />
        <!-- <ReachUsForm class="w-1/2"/> -->
        <!-- LAND -->
    </Animatable>
</template>