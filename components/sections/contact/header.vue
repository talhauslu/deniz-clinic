<template>
    <section class="w-full flex flex-col items-center gap-8 p-16">
        <div class="flex flex-col gap-4 items-center w-full">
            <h1 class="text-5xl font-semibold ">Bize ulaşın</h1>
            <span class="font-light">En uygun tedaviyi beraber belirleyelim</span>
        </div>
        <div class="flex flex-row justify-around w-auto md:w-2/3 gap-4 md:gap-0 flex-wrap">

            <a href="mailto:denizyilmaz@gmail.com" class="flex flex-col items-center gap-4 flex-1">
                <div
                    class="flex justify-center items-center text-center rounded-full  bg-black text-white hover:bg-pink-400 border transition h-24 w-24">
                    <i :class="`fa-solid fa-envelope text-3xl`"></i>
                </div>
                <h2 class="text-logorange tracking-wider font-semibold">EMAIL</h2>
                <span>denizyilmaz@gmail.com</span>
            </a>

            <a href="tel:+905433703209" class="flex flex-col items-center gap-4 flex-1">
                <div
                    class="flex justify-center items-center text-center rounded-full bg-black text-white hover:bg-pink-400 border transition h-24 w-24">
                    <i :class="`fa-solid fa-phone text-3xl`"></i>
                </div>
                <h2 class="text-logorange tracking-wider font-semibold">TELEFON</h2>
                <span>+90 543 370 32 09</span>
            </a>

            <a href="https://wa.me/+905433703209" target="_blank" class="flex flex-col items-center gap-4 flex-1">
                <div
                    class="flex justify-center items-center text-center rounded-full bg-black text-white hover:bg-pink-400 border transition h-24 w-24">
                    <i :class="`fa-brands fa-whatsapp text-3xl`"></i>
                </div>
                <h2 class="text-logorange tracking-wider font-semibold">WHATSAPP</h2>
                <span>Bize mesaj atın</span>
            </a>

            <a href="https://www.facebook.com" target="_blank" class="flex flex-col items-center gap-4 flex-1">
                <div
                    class="flex justify-center items-center text-center rounded-full bg-black text-white hover:bg-pink-400 border transition h-24 w-24">
                    <i :class="`fa-brands fa-facebook text-3xl`"></i>
                </div>
                <h2 class="text-logorange tracking-wider font-semibold">FACEBOOK</h2>
                <span>Bizi takip edin</span>
            </a>

            <a href="https://www.instagram.com/dr.denizyilmaz" target="_blank" class="flex flex-col items-center gap-4 flex-1">
                <div
                    class="flex justify-center items-center text-center rounded-full bg-black text-white hover:bg-pink-400 border transition h-24 w-24">
                    <i :class="`fa-brands fa-instagram text-3xl`"></i>
                </div>
                <h2 class="text-logorange tracking-wider font-semibold">INSTAGRAM</h2>
                <span>Bizi takip edin</span>
            </a>

        </div>
    </section>

</template>