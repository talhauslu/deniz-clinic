<script>
import Landing from '../components/sections/services/Landing.vue';
import Animatable from '../components/animation/animatable.vue';
import Introduction from '../components/sections/before-after/Introduction.vue';
import BeforeAfter from '../components/BeforeAfters.vue';
import ReachUs from '../components/ReachUs.vue';
export default {
  components: {
    Landing,
    Animatable,
    Introduction,
    BeforeAfter,
    ReachUs
},
  data() {
    return {
      bas: [
        {
          before: {
            image: "/before.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile.",

          },
          after: {
            image: "/after.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima necessitatibus impedit quasi veniam nam deserunt neque debitis ducimus corrupti dolorem exercitationem atque."
        },
        {
          before: {
            image: "/before.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          after: {
            image: "/after.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima necessitatibus impedit quasi veniam nam deserunt neque debitis ducimus corrupti dolorem exercitationem atque."
        },
        {
          before: {
            image: "/before.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          after: {
            image: "/after.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima necessitatibus impedit quasi veniam nam deserunt neque debitis ducimus corrupti dolorem exercitationem atque."
        },
        {
          before: {
            image: "/before.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          after: {
            image: "/after.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima necessitatibus impedit quasi veniam nam deserunt neque debitis ducimus corrupti dolorem exercitationem atque."
        }
      ]
    }
  }
}
</script>

<template>
  <Animatable>
    <Landing image="/before-after-landing.jpg" title="Önce & Sonra" />
    <Introduction />
    <BeforeAfter :before_afters="bas" />
    <ReachUs/>
  </Animatable>
</template>
