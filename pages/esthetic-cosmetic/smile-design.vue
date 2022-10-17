<script>
import Landing from '../../components/sections/services/Landing.vue';
import Animatable from '../../components/animation/animatable.vue';
import Introduction from '../../components/sections/services/Introduction.vue';
import CheckMarks from '../../components/sections/services/CheckMarks.vue';
import ShortDescription from '../../components/sections/services/ShortDescription.vue';
import Description from '../../components/sections/services/Description.vue';
import ReachUsForm from '../../components/ReachUsForm.vue';
import ReachUs from '../../components/ReachUs.vue';
export default {
    components: { Landing, Animatable, Introduction, CheckMarks, ShortDescription, Description, ReachUs }
}
</script>

<template>
    <Animatable>
        <Landing image="/woman-with-perfect-smile-whitening-teeth-veneers-v-2LCEPRP.webp" title="GÜLÜŞ TASARIMI" />
        <Introduction heading="Gerçek gülüşünü ortaya çıkar" content="Gülüş tasarımı denilince akla ilk yaprak porselen dişler gelse de, çoğu durumlarda
                yalnızca diş eti estetiği, dudak estetiği, diş temizliği ve diş beyazlatması, ve dişlerdeki çapraşıklıkların
                düzenlenmesi için ortodontik tedavilerle istenilen gülüş yakalanabilir."
            image="/smile-design-landing.jpg" />
        <Description image="/attractive-african-woman-with-perfect-skin-smiling-E4ENK2Q.webp" :left="false" heading="Gülüş Tasarımı nedir?"
            :content="['Her hastanın estetik gereksinimleri farklı olacağından uygulanacak işlemler kişiye özel olarak planlanır. Bu işlemler belirlenirken hastanın; yüz hatları, cinsiyeti, yaşı ve beklentileri gibi faktörler dikkate alınır. Gülüş tasarımı bu bütünü tamamlayan ve hastaya istediği estetik görünümü ve fonksiyonu kazandırmayı amaçlayan tasarım olarak ifade edilebilir. Bu da çeşitli nedenlerle estetik açıdan görünümü bozulan dişler ve diş etlerinin doğal ve güzel bir görünüme kavuşmasını sağlayarak gerçekleştirilir.', 'Yapılan gülüş dizaynı sonucunda, dişler (Beyaz Estetik) ve diş etlerinde (Pembe Estetik) uygun olan değişikliklerin, hangi miktarda ve nasıl yapılması gerektiği saptanır ve bu planlama sonucu estetik diş hekimliği uygulamalarına geçilir.']" />
        <CheckMarks />
        <ShortDescription />
        <ReachUs/>
    </Animatable>
</template>