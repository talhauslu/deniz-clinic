<script>
import Landing from '../components/sections/services/Landing.vue';
import Animatable from '../components/animation/animatable.vue';
import Introduction from '../components/sections/services/Introduction.vue';
import CheckMarks from '../components/sections/services/CheckMarks.vue';
import ShortDescription from '../components/sections/services/ShortDescription.vue';
import Description from '../components/sections/services/Description.vue';
import ReachUsForm from '../components/ReachUsForm.vue';
import ReachUs from '../components/ReachUs.vue';
import QandA from '../components/sections/services/QandA.vue';
export default {
    components: { Landing, Animatable, Introduction, CheckMarks, ShortDescription, Description, ReachUs, QandA }
}
</script>

<template>
    <Animatable>
        <Landing image="/white-teeth.jpg" title="Diş Beyazlatma (Bleaching)" />
        <Introduction class="bg-white" heading="İdeal diş beyazlığına eriş"
            content="Diş beyazlatma dişlerin rengini açma işlemidir. Genetik ya da çeşitli nedenlerle diş minesinin rengi değişir. Diş beyazlatma dişin içindeki kromojenlerin kimyasal olarak değişmesidir.
        Dişlerin yüzeyindeki mine yapısında oluşan renkli organik ve inorganik maddelerin diş beyazlatma jelleri ile giderildiği kozmetik bir çözümdür."
            image="/man-holding-mockup-teeth.jpg" />
        <Description image="/dentist-table.jpg" :left="false" heading="Diş beyazlatma kalıcı mıdır?"
            :content="[
            {list:false, texts:['Kalıcı diş beyazlatma işlemi, çeşitli nedenlerle renk değiştirmiş ve sararmış dişlerin rengini açmak için uygulanmaktadır. Diş beyazlatma kalıcı mıdır? Sorusunun cevabı ise pek çok farklı etkene bağlıdır. Kişinin diş ve mine, dentin yapısı (diş alt rengi), kullandığı ilaçlar, kahve ve sigara kullanımı ile ağız hijyen ve bakımına temizliğine özen gösterme durumunda bağlı olarak diş beyazlatmanın kalıcılığı değişecektir. Kalıcı diş beyazlatma sürecinde kişilere büyük görev düşmektedir.', 'Kalıcı diş beyazlatma istendiğinde mutlaka lazerle tedavi seçeneği tercih edilmelidir. Diş beyazlatma işlemi için uzman estetik diş hekimlerinden destek almalısınız.']},]" />
        <CheckMarks :content="[
            {icon_class:'', subheading:'Doğru Method', content:'Kalıcı diş beyazlatma istendiğinde mutlaka lazerle tedavi seçeneği tercih edilmelidir.'},
            {icon_class:'', subheading:'Doğru Ürün', content:'Beyazlığın kalıcılığı için hekim tarafından tavsiye edilen ürünler kullanılmalıdır.'},
            {icon_class:'', subheading:'Düzenli Kontrol', content:'Hekiminiz tarafından düzenli kontrol diş beyazlığında kalıcılık için yapılacak işlemlerin belirlenmesinde önemlidir.'},
            {icon_class:'', subheading:'Hijyenik Bakım', content:'Kullanılan ilaçlar, kahve ve sigara kullanımı ile ağız hijyeni kalıcı beyazlıkta büyük öneme sahiptir.'},
        ]" />
        <ShortDescription
            content="Hekimimiz tarafından ofis beyazlatma ve ev tipi sistemler ile uygulanmasında hiçbir zarar bulunmamaktadır. Ancak bilinçsizce kullanılan diş beyazlatma ürünlerinin diş hassasiyetinizi ciddi miktarda arttırabileceği için yarardan çok zararlı etkiye sahip olabileceği unutulmamalıdır."
            heading="Diş Beyazlatma" />
        <QandA :qas="[
            {q:'Diş beyazlatmayı ne kadar aralıklarla yaptırabilirim ?', a:'Dişlerin tekrar eski renklerine dönmeden 6 ayda bir düzenli kontroller sağlanarak gerektiği takdirde beyazlatma işleminin 6 ayda veya yılda bir tekrarlanması, beyazlığın daha kalıcı olması açısından değerlendirilebilir.', visible:false}
        ]" />
        <ReachUs />
    </Animatable>
</template>