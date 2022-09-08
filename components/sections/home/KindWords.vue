<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    components: { VueSlickCarousel },
    data() {
        return ({
            comments: [
                {
                    tr: "Uzun araştırmalarım neticesinde deniz Yılmaz hocamla tanışmış olmaktan mutluluk duyuyorum küçüklüğümden kalma dişçi fobimi yenmemi kesinlikle kendisine borçluyum Güler yüzü sıcak kanlı tavırlarıyla kendimi evimdeymişcesine rahat hissettim teşekkürler deniz hocam 🙏☺️",
                    en: "As a result of my long researches, I am happy to have met my teacher, Deniz Yılmaz. I definitely owe it to him that I overcame my dentist phobia from my childhood. I felt comfortable with his smiling face and warm-blooded demeanor, thank you Deniz, teacher 🙏☺️",
                    author: "Sedat"
                }, {
                    tr: "Sadece yaptığı işin kalitesi ile değil aynı zamanda güler yüzü ve muhabbeti ile çok güzel bir insan 👏👏",
                    en: "He is a very beautiful person not only with the quality of his work but also with his smiling.",
                    author: "Emrecan"
                }, {
                    tr: "İstanbul’daki en iyi diş hekimi diyebilirim 👌🏼Herkese tavsiye💞",
                    en: "I can say she is the best dentist is Istanbul. I recommend her to everyone.",
                    author: "Aslı"
                }, {
                    tr: "Deniz hocam sayesinde dişlerim inci gibi oldu.Muayehanesi o kadar güzel ki her detayı huzur verici.İnanılmaz rahat bir şekilde tedavinizi güvenli bir ortamda tamamlıyorsunuz.Dişleri ile problemi olan herkese gönül rahatlığıyla tavsiye ediyorum.",
                    en: "Thanks to Dr. Deniz, my teeth became like pearls. His clinic is so beautiful and every detail is peaceful. You complete your treatment in a safe environment in an incredibly comfortable way. I recommend it to anyone who has problems with their teeth.",
                    author: "Ebrar"
                }
            ]

        })
    }
};
</script>

<template>
    <section class="flex flex-col md:flex-row justify-around items-center p-4">
        <div class="flex flex-col items-center justify-center w-full md:w-1/2">
            <div class="flex flex-col items-center justify-around gap-8 text-4xl text-center">
                <!-- <i class="fa-solid fa-quote-left self-start"></i> -->
                <i class="fa-solid fa-message"></i>
                <h1 class="">Hastalarımızın geri dönüşleri bizim için çok önemli</h1>
                <!-- <i class="fa-solid fa-quote-right self-end"></i> -->

            </div>
        </div>
        <div class="w-full md:w-1/3 p-4">
            <i class="fa-solid fa-quote-left self-start"></i>
            <VueSlickCarousel class="p-4 m-4 border border-gray-300 shadow-lg rounded" :autoplay="true" :arrows="true"
                :dots="false">
                <div v-for="comment of comments">
                    <h1 class="text-2xl mb-4">{{comment.author}}</h1>
                    <p class="">{{comment.tr}}</p>
                </div>
            </VueSlickCarousel>
            <i class="fa-solid fa-quote-right float-right"></i>
            <a class="self-start text-center"
                href="https://www.google.com/search?q=Uzm.+Dr.+Deniz+Y%C4%B1lmaz&sxsrf=ALiCzsZzFKpVeH-Xsrb6UXKK16jqfZFu4A%3A1662583508997&ei=1AIZY8y-PLuFxc8Pos-QgAQ&ved=0ahUKEwjM-NmbxoP6AhW7QvEDHaInBEAQ4dUDCA4&uact=5&oq=Uzm.+Dr.+Deniz+Y%C4%B1lmaz&gs_lcp=Cgdnd3Mtd2l6EAMyBggAEB4QFjIGCAAQHhAWOgQIIxAnOgsILhDHARDRAxCRAjoFCAAQgAQ6DgguEIAEEMcBENEDENQCOgsILhCABBDHARDRAzoICC4QgAQQ1AI6BQguEIAEOgsILhCABBDHARCvAToFCAAQywE6CwguEMcBEK8BEMsBOgoILhDHARCvARATOggIABAeEBYQEzoFCAAQhgNKBAhBGAFKBAhGGABQzQlYgitg0y1oA3AAeACAAZICiAGzHZIBBjAuMTYuNZgBAKABAcABAQ&sclient=gws-wiz#lrd=0x14cab7b4431dcb6d:0xc3a5f8c70b1509d3,1,,,">
                <h1 class="text-xl underline ">Bütün yorumları gör.</h1>
                <div class="text-yellow-400  text-center">
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                </div>
            </a>
        </div>
    </section>
</template>