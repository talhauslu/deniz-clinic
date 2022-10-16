<script>
import Animation from './animation';
import { onMounted, onUnmounted } from 'vue';
export default {
    setup() {
        var animatables = []

        function onScroll() {
            Animation.updateClasses(animatables)
        }

        onMounted(() => {
            animatables = Array.from(document.getElementsByClassName("animation-element"))
            Animation.setInitialClasses(animatables)
            Animation.updateClasses(animatables)
            document.addEventListener("scroll", onScroll)
        })
        onUnmounted(() => {
            document.removeEventListener("scroll", onScroll)
        })
    }
}
</script>
    
<template>
    <div class="overflow-hidden flex flex-col" id="animatable">
        <slot/>
    </div>
</template>

    