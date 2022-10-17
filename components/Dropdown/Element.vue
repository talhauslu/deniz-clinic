<script>
export default {
    props: {
        title: { type: String, required: true, default: "" },
        hasSubMenu: { type: Boolean, required: false, default: false },
        to:{ type: String, required: false, default:"/" }
    },
    data() {
        return {
            submenuOpen: false
        }
    }
}
</script>

<template>
    <div @mouseenter="submenuOpen = true" @mouseleave="submenuOpen = false"
        class="relative bg-white hover:bg-pink-100 cursor-pointer w-60">
        <NuxtLink :to="to" :class="{'justify-between':hasSubMenu}" class="flex flex-row w-full h-full p-4 items-center">
            <span >{{title}}</span>
            <i v-if="hasSubMenu" class="fa-solid fa-sort-up transform rotate-90"></i>
        </NuxtLink>

        <div v-if="hasSubMenu && submenuOpen" class="absolute top-0 -right-60 float-right border-l z-10 ">
            <slot />
        </div>
    </div>
</template>