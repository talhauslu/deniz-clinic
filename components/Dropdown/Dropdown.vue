<script>
export default {
    props: {
        title: { type: String, required: true, default:"" },
    }
}
</script>

<template>
    <div class="relative group cursor-pointer ">
        <div class=" relative flex flex-row align-center justify-center gap-2 ">
            <span>{{title}}</span>
            <i class="fa-solid fa-sort-down"></i>
        </div>
        <div
            class="flex absolute invisible opacity-0 group-hover:visible group-hover:opacity-100 transition duration-400 flex-col align-center left-0 right-0">
            <slot/>
        </div>
    </div>
</template>