<script>
import Animatable from './../components/animation/animatable.vue'
import Landing from '../components/sections/services/Landing.vue';
import Description from '../components/sections/services/Description.vue';
import ShortDescription from '../components/sections/services/ShortDescription.vue';
import Introduction from '../components/sections/services/Introduction.vue';
import ReachUs from '../components/ReachUs.vue';
import CheckMarks from '../components/sections/services/CheckMarks.vue';

export default {
    components: { Animatable, Landing, Description, ShortDescription, Introduction, ReachUs, CheckMarks }
}
</script>

<template>

    <Animatable>
        <Landing image="/dentist-taking-dental-filling-from-spatula-to-carver.webp" title="İnlay & Onlay" />
        <Introduction heading="Diş çürüklerine yenilikçi çözümler"
            content=" Inlay ve Onlay, yeni bir protez kullanmadan dişte oluşan çürükleri restore etmek için kullanılan diş tedavileri türleridir. Bu tedaviler, yapbozun bir parçası gibi dişin geri kalan kısmına yerleştikleri için dişlerin daha doğal korunmasına yardımcı olur."
            image="/white-teeth.webp" />
        <CheckMarks heading="Inlay & Onlay kaplamaların avantajları" :content="[
            { subheading: 'Güçlü', content: 'Geleneksel dolgulara göre dişin gücünü daha çok arttırırlar.' },
            { subheading: 'Kullanışlı', content: 'Diş hasarı geniş olmadığında krona iyi bir alternatiftir.' },
            { subheading: 'Dayanıklı', content: 'Zamanla renk değiştirmezler.' },
            { subheading: 'Estetik', content: 'Amalgam dolgulara göre daha iyi estetik görünüm sağlar.' },
        ]" />
        <Description image="/inlay-onlay-description.jpg" :left="false" heading="Neden tercih edilir?"
            :content="[
            { list: false, texts: ['Büyük çürüklü dişlerde yapılacak klasik kompozit dolgular kırılgan olabilmektedir. Bu tip dişlerde kron restorasyonu yapabilmek için kalan sağlıklı diş dokusunu da aşındırmak gerekir. Bu nedenle kalan sağlıklı diş dokusunu korumak için inlay ve onlay porselen dolgular geliştirilmiştir. Normal dolgulara göre daha dayanıklı ve uzun ömürlü olan porselen inley ve onley dolgular diş ile iyi bir uyum sağlar.', 'İnleyler ve onleyler normalde kompozit reçine dolgularla sabitlenemeyecek kadar büyük olabilen dişlerin hasarlı kısımlarını onarmak için yapılırken, hasar bir diş kronu gerektiren aşırı derecede geniş değildir.'] }]" />
        <ShortDescription heading="Inley ve onley farkı"
            content="İnleyler geleneksel dolgulara benzer, ancak tüm iş dişin çiğneme yüzeyindeki çıkıntılar içindedir. Onleyler, bir veya daha fazla tüberkül kaplayan inleylerden daha kapsamlıdır. Onleylere bazen kısmi kronlar denir. Kaplamalar, onleylerden dışa doğru uzanır." />
        <ReachUs />
    </Animatable>

</template>