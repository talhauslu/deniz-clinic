<script>
import Landing from '../components/sections/about/Landing.vue';
import { onMounted, onUnmounted } from 'vue'
    export default{
        components:{
            Landing
        },
        setup() {
        function isElemVisible(el) {
            var rect = el.getBoundingClientRect()
            var elemTop = rect.top + 150 // buffer
            var elemBottom = rect.bottom
            return elemTop < window.innerHeight && elemBottom >= 0
        }

        var animatables = []

        function updateClasses() {
            for (var elem of animatables) {
                if (isElemVisible(elem)) {
                    if (elem.className.includes("fade-left")) {
                        elem.className = elem.className.replace("transform -translate-x-10 opacity-0", "transform -translate-x-0 opacity-100")
                    }
                    else if (elem.className.includes("fade-right")) {
                        elem.className = elem.className.replace("transform translate-x-10 opacity-0", "transform translate-x-0 opacity-100")
                    }
                    else if (elem.className.includes("fade-up")) {
                        elem.className = elem.className.replace("transform -translate-y-10 opacity-0", "transform -translate-y-0 opacity-100")
                    }
                    else if (elem.className.includes("fade-down")) {
                        elem.className = elem.className.replace("transform translate-y-10 opacity-0", "transform translate-y-0 opacity-100")

                    }
                }
            }
        }

        function setInitialClasses(){
            for (var elem of animatables) {
                if (elem.className.includes("fade-left")) {
                    elem.className = elem.className + " transform -translate-x-10 opacity-0 transition-all duration-700"
                }
                else if (elem.className.includes("fade-right")) {
                    elem.className = elem.className + " transform translate-x-10 opacity-0 transition-all duration-700"
                }
                else if (elem.className.includes("fade-up")) {
                    elem.className = elem.className + " transform -translate-y-10 opacity-0 transition-all duration-700"
                }
                else if (elem.className.includes("fade-down")) {
                    elem.className = elem.className + " transform translate-y-10 opacity-0 transition-all duration-700"
                }
            }
        }

        onMounted(() => {
            animatables = Array.from(document.getElementsByClassName("animation-element"))
            setInitialClasses()
            updateClasses()
            document.addEventListener("scroll", updateClasses)
        })

        onUnmounted(() => {
            document.removeEventListener("scroll", updateClasses)
        })
    }
    }
</script>

<template>
    <main>
        <Landing/>
        LAND
    </main>
</template>