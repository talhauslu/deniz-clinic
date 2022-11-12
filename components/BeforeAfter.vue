<script>
export default {
    props: {
        before_afters: {
            type: Array,
            required: true,
            default: [
                {
                    before: {
                        image: "/before.jpeg",
                        content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
                    },
                    after: {
                        image: "/after.jpeg",
                        content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
                    }
                }
            ]
        }
    },
    data(){
        return{
            before:false,
            after:false
        }
    }
}
</script>

<template>
    <section class="flex flex-col p-4 items-center text-center w-full gap-8">
        <div class="w-full md:w-auto">
            <h1 class="text-4xl font-light px-8 text-gray-900">Önce & Sonra</h1>
            <div class="h-px w-full bg-gray-500"></div>
        </div>
        <div v-for="ba in before_afters" :key="ba.before.image" class="flex flex-col md:flex-row justify-center gap-8 w-full text-sm">
            <div @mouseover="before = true" @mouseleave="before = false" class="relative h-56 w-full md:w-1/3">
                <nuxt-img class="absolute w-full h-full object-cover" :src="ba.before.image" />
                <div :class="{'hidden':!after, 'flex':after}" class="z-10 relative w-full h-full bg-gray-300 text-black p-8 flex flex-col justify-around text-right">
                    <h1 class="text-base font-semibold">
                        <span>Sonra</span>
                        <i class="hidden md:inline fa-solid fa-circle-arrow-right"></i>
                    </h1>
                    <span>{{ ba.after.content }}</span>
                </div>
            </div>
            <div @mouseover="after = true" @mouseleave="after = false" class="relative h-56 w-full md:w-1/3">
                <nuxt-img class="absolute w-full h-full object-cover" :src="ba.after.image" />
                <div :class="{'hidden':!before, 'flex':before}" class="z-10 relative w-full h-full bg-gray-300 text-black p-8 flex flex-col justify-around text-left">
                    <h1 class="text-base font-semibold">
                        <i class="hidden md:inline fa-solid fa-circle-arrow-left"></i>
                        <span>Önce</span>
                    </h1>
                    <span>{{ ba.before.content }}</span>
                </div>
            </div>
        </div>
    </section>
</template>