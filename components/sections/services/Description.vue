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
        left: { type: Boolean, required: true, default:true },
    }
}
</script>

<template>
    <section :class="{'flex-col md:flex-row':left, 'flex-col-reverse md:flex-row-reverse':!left}" class="flex gap-4 bg-gray-50 p-2 md:p-8">
        <div :class="{'fade-left':left, 'fade-right':!left}" class="w-full md:w-1/2 flex flex-col justify-center gap-8 p-8 animation-element">
            <span>
                <h1 class="text-3xl font-semibold">
                    {{heading}}
                </h1>
                <div class="h-0.5 w-full bg-black"></div>
            </span>
            <p v-for="text of content">
                {{text}}
            </p>
        </div>
        <nuxt-img :class="{'fade-right':left, 'fade-left':!left}" class="w-full md:w-1/2 rounded object-cover animation-element" :src="image" />
    </section>
</template>