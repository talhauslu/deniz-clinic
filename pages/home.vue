<script setup>

</script>

<template>
    <div class="flex flex-row w-full overflow-hidden relative justify-between h-80vh">
        <div class="flex flex-col justify-center gap-8 w-1/2 px-8">
            <h1 class="text-7xl text-gray-700 font-semibold">Sağlıkta dönüşümü keşfet</h1>
            <h2 class="text-4xl">Gülmek her şeyin başıdır</h2>
            <button
                class="inline self-start p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all">
                Randevu Al
            </button>
        </div>
        <video class="absolute right-0 object-cover w-1/2 h-full object-center" autoplay muted loop id="myVideo">
            <source src="/entrance_video.mp4" type="video/mp4">
        </video>
    </div>
</template>