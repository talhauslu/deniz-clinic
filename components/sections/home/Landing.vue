<script>

</script>

<template>
    <section class="flex flex-row w-full overflow-hidden relative justify-between h-80vh min-h-80vh">
        <transition appear name="swipe-from-left">
            <div
                class="flex flex-col justify-between 500:justify-around sm:justify-center sm:gap-8 w-full sm:w-1/2 h-full p-2 sm:p-8 z-10">
                <h1 class="text-white lg:text-gray-600 font-semibold">Sağlıkta dönüşümü keşfet</h1>
                <h2 class="text-white lg:text-black">İyi bir gülüş, iyi bir hayat </h2>
                <button
                    class="inline self-start p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all shadow-md">
                    Randevu Al
                </button>
            </div>
        </transition>
        <transition appear name="swipe-from-right">
            <video
                class="hidden lg:block absolute right-0 object-cover w-1/2 h-full object-center -z-10 border border-white"
                autoplay muted loop id="myVideo">
                <source src="~/assets/media/entrance_video.mp4" type="video/mp4">
            </video>
        </transition>
        <div class="w-full h-full block lg:hidden absolute bg-black">
            <nuxt-img class="object-cover w-full h-full object-center opacity-80" src="/smiling_girl.jpg" />
        </div>
    </section>
</template>

<style scoped>
h1 {
    font-size: 8vh;
}

h2 {
    font-size: 4vh
}
</style>