<script>
export default {
    props: {
        image: { type: String, required: true, default: "" },
        title: { type: String, required: true, default: "" }
    }
}
</script>

<template>
    <section class="w-full h-screen sm:h-90vh relative">
        <nuxt-img class="w-full h-full object-cover absolute" :src="image" />
        <div
            class="w-full h-full flex items-center text-center justify-center relative text-5xl font-extralight text-white bg-black bg-opacity-75">
            <span class="animation-element fade-up">{{title}}</span>
        </div>
    </section>
</template>