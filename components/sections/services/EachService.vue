<script>
export default {
    props: {
        header: { required: true, type: String, default:"Header" },
        image_uri: { required: true, type: String }
    }
}
</script>

<template>
    <div
        class="animation-element w-72 fade-up flex flex-col items-center text-center max-w-max gap-4 p-4 border shadow transition duration-400 mb-4 cursor-pointer bg-gray-50 hover:bg-gray-100">
        <h1 class="text-3xl font-light">
            {{header}}
        </h1>
        <nuxt-img class="h-72 w-64 object-cover rounded" :src="image_uri" />
    </div>
</template>