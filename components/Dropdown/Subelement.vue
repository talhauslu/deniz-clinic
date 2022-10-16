<script>
export default {
    props: {
        title: { type: String, required: true, default: "" },
        to: { type: String, required: true, default: "/" }
    }
}
</script>

<template>
    <NuxtLink :to="to">
        <div class="bg-white hover:bg-pink-100 p-4 w-60">
            {{title}}
        </div>
    </NuxtLink>
</template>