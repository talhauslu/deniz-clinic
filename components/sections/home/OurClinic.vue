<template>
    <section class="w-full h-screen flex justify-center items-center relative">
        <div class="w-11/12 h-5/6 overflow-hidden relative">
            <div id="main" class="w-full h-full group bg-center">
                    <!-- hover:bg-white hover:bg-opacity-40 hover:text-black text-white -->
                <!-- <div class="w-full h-full absolute flex justify-center items-center z-10 text-white bg-black bg-opacity-40 hover:bg-white hover:bg-opacity-40 hover:text-black ">
                    KLİNİK
                </div> -->
                <div class="z-10 bottom-0 top-0 left-0 right-0 absolute flex justify-center items-center tranisition-all duration-500 text-white text-2xl bg-black bg-opacity-40 group-hover:bg-opacity-25">
                    <span>KLİNİĞİMİZ</span>
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