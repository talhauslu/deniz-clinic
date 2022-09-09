<template>
    <section class="w-full h-screen flex justify-center items-center relative">
        <div data-aos="fade-up" class="w-4/5 h-5/6 overflow-hidden relative  cursor-pointer shadow-lg">
            <div id="main" class="w-full h-full group bg-center">
                <div class="z-10 bottom-0 top-0 left-0 right-0 absolute flex justify-center items-center tranisition-all duration-500  bg-black bg-opacity-40 group-hover:bg-opacity-25">
                    <span class="text-white text-3xl font-semibold">KLİNİĞİMİZ</span>
                </div>
               
            </div>
        </div>
    </section>
</template>

<style>
#main {
    background-image: url(./../../../static/akmerkez.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    transition: 500ms;
}
#main:hover{
    scale: 1.1;
}
</style>