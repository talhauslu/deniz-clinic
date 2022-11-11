<script>
export default {
    props: {
        heading: { type: String, required: true, default: "Heading" },
        content: {
            type: Array, required: true, default:
                ["Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia ratione voluptatum repellat providentautem adipisci quaerat repellendus vel modi nemo blanditiis recusandae voluptatem, deserunt odio minusinventore tempore nostrum ad?",
                    "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia ratione voluptatum repellat providentautem adipisci quaerat repellendus vel modi nemo blanditiis recusandae voluptatem, deserunt odio minusinventore tempore nostrum ad?"]
        },
        image: { type: String, required: true, default: "/veneers.png" },
        left: { type: Boolean, required: true, default: true },
        list: { type: Boolean, required: false, default: false },
    }
}
</script>

<template>
    <section :class="{'flex-col-reverse md:flex-row':left, 'flex-col-reverse md:flex-row-reverse':!left}"
        class="flex bg-gray-50 justify-around">
        <div :class="{'fade-left':left, 'fade-right':!left}"
            class="w-full md:w-1/2 flex flex-col justify-center gap-8 p-8 animation-element">
            <span>
                <h1 class="text-3xl font-semibold">
                    {{heading}}
                </h1>
                <div class="h-0.5 w-full bg-black"></div>
            </span>
            <div v-for="content_ of content">
                <ul class="flex flex-col gap-4" v-if="content_.list">
                    <li v-for="text in content_.texts">
                        • {{text}}
                    </li>
                </ul>
                <div class="flex flex-col gap-4" v-else>
                    <span v-for="text in content_.texts">
                        {{text}}
                    </span>
                </div>
            </div>
        </div>
        <nuxt-img :class="{'fade-right':left, 'fade-left':!left}"
            class="w-full md:w-1/2 h-40vw rounded object-cover animation-element" :src="image" />
    </section>
</template>