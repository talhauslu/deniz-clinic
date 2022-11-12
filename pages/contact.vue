<script>
import Animatable from '../components/animation/animatable.vue';
import Header from '../components/sections/contact/header.vue';
import ReachUs from '../components/ReachUs.vue';
export default {
    components: {
        Animatable, Header, ReachUs
    },
}
</script>

<template>
    <Animatable>
        <Header />
        <ReachUs />
    </Animatable>
</template>