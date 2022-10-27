<script>
import Animatable from './../components/animation/animatable.vue'
import Landing from '../components/sections/services/Landing.vue';
import Description from '../components/sections/services/Description.vue';
import ShortDescription from '../components/sections/services/ShortDescription.vue';
export default {
    components: { Animatable, Landing, Description, ShortDescription }
}
</script>

<template>
    <Animatable>
        <Landing image="/zirconium-landing.jpg" title="ZİRKONYUM KAPLAMA" />
        <Description image="/zirconium-landing.jpg" :left="false" heading="Zirkonyum Kaplama nedir?" :content="[
        {
            list: false, texts: ['Beyaz sert bir metal olan Zirkonyum elementi diş hekimliğinde zirkonya olarak kullanılmaktadır. Çok yüksek kırılma direncine sahip bir restoratif materyaldir. Nikel-titanyum gibi metal elementlere alerjisi olan hastalar için de uygun bir seçimdir.',
                'Işık geçirgenliği, hazırlanabilirliği ve parlatılabilir yapısı sayesinde tüm ön/arka restorasyonların yapımında kullanılabilir. Doku dostu olması nedeniyle diş hekimliğinde tercih edilen restorasyon materyallerinden biridir.'
            ]
        }]" />

        <Description image="/zirconium-landing.jpg" :left="true" heading="Zirkonyum Kaplamalar kimlere uygulanabilir?" :content="[
        {
            list: true, texts: ['Daha önce kaplama tedavisi yapılmış kesilmiş dişlerde',
                'Kırık dişlerin düzeltilmesinde',
                'Ayrılmış dişlerin birleştirilmesinde',
                'Rengi değişmiş ve yapısı bozulmuş eski dolguların revizyonunda',
                'Çapraşık ve eğilmiş dişlerin tedavisinde',
                'Dolgu yapılması mümkün olmayacak derecede, çok madde kaybetmiş dişlerde kullanılarak olumlu sonuçlar alınmaktadır'
            ]
        }]" />
                <ShortDescription
            content="Klasik metal alt yapılı porselen yerine ışık geçirgenliğinin yüksek olması nedeniyle daha doğal bir görünüm elde edilir. "
            heading="Zirkonyum kaplamalarda," />

    </Animatable>
</template>