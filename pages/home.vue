<script setup>

</script>

<template>
    <div class="flex flex-row w-full overflow-hidden relative justify-between h-80vh">
        <div class="flex flex-col justify-between 500:justify-around sm:justify-center sm:gap-8 w-full sm:w-1/2 h-full py-8 sm:py-0 px-8 z-10">
            <h1 class="text-5xl sm:text-7xl text-white sm:text-gray-600 font-semibold">Sağlıkta dönüşümü keşfet</h1>
            <h2 class="text-2xl sm:text-4xl text-white sm:text-black">İyi bir gülüş, iyi bir hayat </h2>
            <button
                class="inline self-start p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all">
                Randevu Al
            </button>
        </div>
        <video class="hidden sm:block absolute right-0 object-cover w-1/2 h-full object-center -z-10 border border-white" autoplay muted loop id="myVideo">
            <source src="~/assets/media/entrance_video.mp4" type="video/mp4">
        </video>
        <div class="w-full h-full block sm:hidden absolute bg-black">
            <nuxt-img class=" object-cover w-full h-full object-center 500:object-left opacity-80" 
        src="/smiling_girl.jpg"/>
        </div>
    </div>
</template>