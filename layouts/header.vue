<template>
    <header class="relative z-50 shadow">
        <div class="relative flex flex-col w-full bg-white ">
            <div class="hidden md:flex md:flex-row w-full justify-around text-gray-600 p-3 ">
                <div class="flex flex-row justify-around items-center gap-2">
                    <i class="fa-solid fa-location-dot text-4xl text-pink-200"></i>
                    <div class="text-sm flex flex-col flex-around">
                        <span class="font-semibold">Akmerkez Residence Daire:7B1</span>
                        <span>Beşiktaş/İstanbul</span>
                    </div>
                </div>
                <div class="flex flex-row justify-around items-center gap-2">
                    <i class="fa-solid fa-clock text-4xl text-pink-200"></i>
                    <div class="text-sm flex flex-col flex-around">
                        <span class="font-semibold">Monday - Friday</span>
                        <span>9 AM - 5 PM</span>
                    </div>
                </div>
                <div class="flex flex-row justify-around items-center gap-2">
                    <i class="fa-solid fa-mobile-screen text-4xl text-pink-200"></i>
                    <div class="text-sm flex flex-col flex-around">
                        <span class="font-semibold">+90 530 650 94 33</span>
                        <span>denizyilmaz@xyz.com</span>
                    </div>
                </div>
                <div class="flex flex-row justify-around items-center gap-4 text-2xl text-gray-600 ">
                    <i class="fa-brands fa-instagram cursor-pointer p-2 rounded-full hover:bg-gray-200"></i>
                    <i class="fa-brands fa-linkedin cursor-pointer p-2 rounded-full hover:bg-gray-200"></i>
                    <i class="fa-brands fa-whatsapp cursor-pointer p-2 rounded-full hover:bg-gray-200"></i>
                </div>
            </div>
            <div class="flex flex-row w-full justify-between px-6 py-2 bg-opacity-60 items-center bg-indigo-50">

                <nuxt-img src="/logo-removebg-preview.png" class="object-contain h-20"></nuxt-img>

                <div class="flex flex-row items-center gap-8">
                    <nav class="flex flex-row gap-8 font-bold uppercase text-gray-600 text-sm">
                        <NuxtLink to="/slm">ANA SAYFA</NuxtLink>

                        <div class="relative group">
                            <NuxtLink class=" relative flex flex-row align-center gap-2" to="/slm">
                                <span>HİZMETLERİMİZ</span>
                                <i class="fa-solid fa-sort-down"></i>
                            </NuxtLink>
                            <div class="flex absolute invisible mt-1 opacity-0 group-hover:visible group-hover:opacity-100 transition duration-400 w-full flex-col align-center bg-blue-200">
                                <div><span>SLM</span></div>
                                <div><span>SLM</span></div>
                                <div><span>SLM</span></div>
                                <div><span>SLM</span></div>
                                <div><span>SLM</span></div>
                            </div>
                        </div>

                        <NuxtLink to="/slm">HAKKIMIZDA</NuxtLink>
                        <NuxtLink to="/slm">BLOG</NuxtLink>
                        <NuxtLink to="/slm">MEDYA</NuxtLink>
                        <NuxtLink to="/slm">İLETİŞİM</NuxtLink>
                    </nav>

                    <button
                        class="p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all">
                        Randevu Al
                    </button>
                </div>
            </div>
        </div>

    </header>
</template>