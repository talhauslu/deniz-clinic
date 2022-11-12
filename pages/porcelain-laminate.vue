<script>
import Landing from '../components/sections/services/Landing.vue';
import Animatable from '../components/animation/animatable.vue';
import Introduction from '../components/sections/services/Introduction.vue';
import CheckMarks from '../components/sections/services/CheckMarks.vue';
import ShortDescription from '../components/sections/services/ShortDescription.vue';
import Description from '../components/sections/services/Description.vue';
import ReachUs from '../components/ReachUs.vue';
import QandA from '../components/sections/services/QandA.vue';
import BeforeAfter from '../components/BeforeAfter.vue';
export default {
    components: { Landing, Animatable, Introduction, CheckMarks, ShortDescription, Description, ReachUs, QandA, BeforeAfter }
}
</script>

<template>
    <Animatable>
        <Landing image="/porcelain-lamina-landing.jpg" title="PORSELEN LAMİNA & LAMINATE VENEERS" />
        <Introduction heading="Daha doğal, daha beyaz."
            content="Laminate Veneer restorasyonlar, Dişlerin sadece ön yüzeylerinden minimal (0.3-0.7 mm) aşındırmalar yaparak, bazı zamanlar ise hiç aşındırma yapmadan sadece ölçü alınarak bu alanlara çok ince porselen diş laminalarının yapıştırılması işlemidir. Yaprak porselen dişler, estetik, güvenli, diş eti irritasyonu yaratma riski az ve konservatif bir tedavidir. Çok ince olmaları sebebiyle ışığın geçirgenliğine izin verirler. Bu nedenle, dişler doğal görünebilmektedir."
            image="/dental-crown.jpg" />
        <Description image="/dentist-table.jpg" :left="false" heading="Laminate Veneer kimlere uygulanır?" :content="[
        {
            list: true, texts: ['Beyazlatma işlemlerinden sonuç alınamadığı ileri derecede renk değiştirmiş dişlere estetik görünüm kazandırmak için',
                'Aşınmış, yapısal formu bozulmuş dişlerin estetik görünümüne kavuşturulması için',
                'Kırık veya aşınmış dişlerin restorasyonunda',
                'Ön dişlerdeki ufak çapraşıkların ve simetri sorunlarının düzeltilmesi için',
                'Uzun yıllar ortodontik tedavi görmek istenilmeyen durumlar için'
            ]
        }]" />
        <ShortDescription
            content="Laminalar iyi ve doğru bir ağız bakımıyla yıllarca sorunsuz olarak kullanılabilirler. Bunu da sebebi diğer yapıştırma sistemlerden daha üstün özelliklere sahip porselenden imal edilmiş olmalarıdır. Lekelenme ve aşınmaya karşı dirençlidirler. Ömürlerini uzatmak için ağız bakımına dikkat etmek gerekir."
            heading="Porselen Lamina & Laminate Veneers" />
        <QandA :qas="[
            { q: 'Hangi durumlarda ve kimlere uygulanamaz?', a: 'Pipo kullanımı kalem ısırması gibi alışkanlıklardan vazgeçilemediği durumlarda ve dişlerde ileri seviyede çapraşıklık olan durumlarda laminate veneer uygulanamaz.', visible: false },
            { q: 'Porselen lamina kaç seans sürer?', a: '10 gün içerisinde 2 seansta tedavinin tamamlanması öngörülür. İlk seans dişlerinize aşındırma işlemi uygulanır ya da aşındırmadan yalnızca ölçüler alınır. 10 gün sonra ikinci randevunuzda laminate veneerler dişlerinize uygulanır.', visible: false },
            { q: 'Porselen lamina düşer mi?', a: 'Laminate veneerler dişlerinize uygulandıktan sonra dişlerinizle bir bütün haline gelir. Bilinenin aksine elma gibi meyveleri ısırarak yiyebilir, kendi dişiniz gibi kullanabilirsiniz.', visible: false },
            { q: 'Porselen lamina dişlerin ömrü ne kadardır?', a: 'Laminalar iyi ve doğru bir ağız bakımıyla yıllarca sorunsuz olarak kullanılabilirler. Bunu da sebebi diğer yapıştırma sistemlerden daha üstün özelliklere sahip porselenden imal edilmiş olmalarıdır. Lekelenme ve aşınmaya karşı dirençlidirler. Ömürlerini uzatmak için ağız bakımına dikkat etmek gerekir. ', visible: false },
            { q: 'Porselen laminalar renk değiştirir mi?', a: 'Laminate veneer dişlerin yüzeyleri porselen, cilalı ve pürüzsüz olduğu için kahve sigara lekesi tutmamaktadır.', visible: false }
        ]" />
        <BeforeAfter/>
        <ReachUs />
    </Animatable>
</template>