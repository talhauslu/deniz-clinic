<template>
    <section class="flex flex-col md:flex-row justify-center pb-4">
        <div class="w-full md:w-1/2 flex items-center justify-center ">
            <form class="flex w-full md:w-2/3 h-full flex-col justify-around gap-4 border p-4 text-gray-700">
                <h1 class="text-2xl font-semibold">Soru sor</h1>

                <div class="w-full flex flex-row justify-between">
                    <label>İsmin:</label>
                    <input class="w-4/5"/>
                </div>
                <div class="w-full flex flex-row justify-between">
                    <label>Email:</label>
                    <input class="w-4/5" />
                </div>
                <div class="w-full flex flex-row justify-between">
                    <label>Mesaj:</label>
                    <textarea rows="4"  class="w-4/5 resize-none" />
                </div>

                <div>
                    <button class="bg-pink-300 border hover:bg-pink-400 transition-all p-2 text-sm">Gönder</button>
                </div>

            </form>
        </div>
        <div class="flex items-center justify-center w-full md:w-2/5">
            <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3007.6627497029776!2d29.025008315376386!3d41.07636397929391!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14cab7b4431dcb6d%3A0xc3a5f8c70b1509d3!2sUzm.%20Dr.%20Deniz%20Y%C4%B1lmaz!5e0!3m2!1sen!2str!4v1662646830852!5m2!1sen!2str"
                class="w-full h-30vw left-0 right-0" style="border:0;" allowfullscreen="" loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
    </section>
</template>