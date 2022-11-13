<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    components: { VueSlickCarousel },
};
</script>

<template>
    <section class="animation-element flex flex-col md:flex-row justify-around items-center p-4 bg-shift-wb text-white relative">
        <nuxt-img class="hidden md:block absolute left-0 top-0 transform -rotate-90" src="/dots-corner.png"></nuxt-img>
        <div class="flex flex-col items-center justify-center w-full md:w-1/2">
            <div class="animation-element fade-left flex flex-col items-center justify-around gap-8 text-4xl text-center">
                <i class="fa-solid fa-message"></i>
                <h1 class="">{{$t('index').kindwords.heading}}</h1>
                <span class="text-sm">
                    <span class="text-yellow-400 text-center">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </span>
                      22 reviews on
                    <nuxt-img class="w-9 object-contain inline" src="/google.png"/>
                </span>
            </div>
        </div>
        <div class="animation-element fade-right w-full md:w-1/3 p-4">
            <i class="fa-solid fa-quote-left self-start"></i>
            <VueSlickCarousel class="p-4 m-4 border border-gray-300 shadow-lg rounded bg-white text-black" :autoplay="true" :arrows="true"
                :dots="false">
                <div v-for="comment of $t('index').kindwords.reviews">
                    <p class="">{{comment.content}}</p>
                    <h1 class="text-xl font-light mt-4 float-right">{{comment.author}}</h1>
                </div>
            </VueSlickCarousel>
            <i class="fa-solid fa-quote-right float-right"></i>
            <a class="self-start text-center"
                href="https://www.google.com/search?q=Uzm.+Dr.+Deniz+Y%C4%B1lmaz&sxsrf=ALiCzsZzFKpVeH-Xsrb6UXKK16jqfZFu4A%3A1662583508997&ei=1AIZY8y-PLuFxc8Pos-QgAQ&ved=0ahUKEwjM-NmbxoP6AhW7QvEDHaInBEAQ4dUDCA4&uact=5&oq=Uzm.+Dr.+Deniz+Y%C4%B1lmaz&gs_lcp=Cgdnd3Mtd2l6EAMyBggAEB4QFjIGCAAQHhAWOgQIIxAnOgsILhDHARDRAxCRAjoFCAAQgAQ6DgguEIAEEMcBENEDENQCOgsILhCABBDHARDRAzoICC4QgAQQ1AI6BQguEIAEOgsILhCABBDHARCvAToFCAAQywE6CwguEMcBEK8BEMsBOgoILhDHARCvARATOggIABAeEBYQEzoFCAAQhgNKBAhBGAFKBAhGGABQzQlYgitg0y1oA3AAeACAAZICiAGzHZIBBjAuMTYuNZgBAKABAcABAQ&sclient=gws-wiz#lrd=0x14cab7b4431dcb6d:0xc3a5f8c70b1509d3,1,,,">
                <h1 class="text-xl underline ">{{$t('index').kindwords.see_all_comments}}</h1>
            </a>
        </div>
    </section>
</template>
