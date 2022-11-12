<script>
import Animatable from './../components/animation/animatable.vue'
import Landing from '../components/sections/services/Landing.vue';
import Description from '../components/sections/services/Description.vue';
import ShortDescription from '../components/sections/services/ShortDescription.vue';
import Introduction from '../components/sections/services/Introduction.vue';
import ReachUs from '../components/ReachUs.vue';
import CheckMarks from '../components/sections/services/CheckMarks.vue';
import QandA from '../components/sections/services/QandA.vue';
import BeforeAfter from '../components/BeforeAfter.vue';
export default {
    components: { Animatable, Landing, Description, ShortDescription, Introduction, ReachUs, CheckMarks, QandA, BeforeAfter }
}
</script>

<template>

    <Animatable>
        <Landing image="/gum-esthetic-landing.jpg" title="Diş Eti Estetiği" />
        <Introduction heading="Küçük detaylar, belirgin sonuçlar"
            content="Gülüş tasarımının en önemli kriterlerinden birisi diş etinin sağlıklı ve seviyelerinin eşit olmasıdır. Kişi kimi zaman sağlıklı dişlere sahip olsa da diş ve diş etlerinin orantısızlığını estetik olarak iyileştirmek isteyebilir.  Bazı diş eti büyümeleri sonucunda dişler daha küçük gözükürken, diş etleri çok fazla gözükür. Böyle durumlarda diş eti estetiği yani pembe estetikle dişlere dokunmadan sadece diş eti düzenlemeleriyle dişlerin büyüklüğü artırabilir. "
            image="/gum-esthetic-introduction.jpg" />
        <ShortDescription heading="İyi bir gülüş için"
            content="Mükemmel bir gülüşe sahip olabilmek için dudaklar, çene, diş formu, diş rengi, dişlerin seviyesi, diş uzunluğu ve boyutu gibi birçok faktörle birlikte diş etinin bir uyum içerisinde olması gerekmektedir." />
        <QandA :qas="[
            { q: 'Kimler diş eti estetiği yaptırmalıdır?', a: 'Hastalar gülümserken dişeti çok fazla açığa çıktığında dişleri olması gerekenden daha küçük görünür. Dişeti şekillendirme yöntemleri ile bu dişler olduğundan çok daha büyük hale getirilebilir. Ayrıca düzensiz diş eti çizgisi olan hastalar da işlem için adaydır.', visible: false },
            { q: 'Diş eti estetiğinin avantajları nelerdir?', a: 'Diş eti estetiğinde diş dokusuna herhangi bir müdahale yapmadan görünüşte büyük değişimler yaratılabilir. Diş uzunluklarının diğerleri ile orantılı olması sağlanabilir. Diş enfeksiyonları giderilir ve tekrar etmemeleri sağlanır. Genel olarak diş eti dokusunda iyileşme sağlanır ve gülüşe olumlu katkıları olur.', visible: false },
            { q: 'Diş eti estetiği sırasında acı hissedecek miyim?', a: 'Lokal anestezi kullanıldığı için hastalar operasyon sırasında neredeyse hiçbir şey hissetmezler. Diş eti cerrahları diş eti çizgisinin düzgün olmasını ve dişlerin yeterince büyük olmasını göz önünde tutarak fazla dişeti dokusunu alırlar. İşlem sırasında ufak kanamalar olabilir ve işlemden sonra soğuk ve sıcak hassasiyeti yaygındır.', visible: false },
            { q: 'Operasyon sonrası nelere dikkat etmeliyim?', a: 'Operasyondan sonra diş etlerinizin sağlıklı hale dönmesi için biraz zaman gerekir. Bu yüzden ilk birkaç gün evde geçirilmesi tavsiye edilir. Aşırı baharatlı ve sert gıdalardan kaçınılması gerekmektedir. Dişçinizin size tarif ettiği şekilde dişler fırçalanmalı ve herhangi bir fazla kanamada veya şişme durumunda haber verilmelidir.', visible: false },
        ]" />
        <BeforeAfter/>

        <ReachUs />
    </Animatable>

</template>