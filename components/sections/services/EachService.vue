<script>
export default {
    props: {
        header: { required: true, type: String, default: "Header" },
        image_uri: { required: true, type: String }
    }
}
</script>

<template>
    <div
        class="relative animation-element h-72 w-80 fade-up flex flex-col border shadow transition duration-400 cursor-pointer group">
        <h1
            class="flex flex-col items-start justify-end text-2xl w-full h-full bg-black bg-opacity-50 text-white relative z-10">
            <span class="text-3xl p-2  w-full group-hover:bg-black group-hover:bg-opacity-50 transition duration-400">{{ header }}</span>
        </h1>
        <nuxt-img class="w-full h-full object-cover absolute" :src="image_uri" />
    </div>
</template>