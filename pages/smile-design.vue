<script>
import Landing from '../components/sections/services/Landing.vue';
import Animatable from '../components/animation/animatable.vue';
import Introduction from '../components/sections/services/Introduction.vue';
import CheckMarks from '../components/sections/services/CheckMarks.vue';
import ShortDescription from '../components/sections/services/ShortDescription.vue';
import Description from '../components/sections/services/Description.vue';
import ReachUs from '../components/ReachUs.vue';
import QandA from '../components/sections/services/QandA.vue';
import BeforeAfters from '../components/BeforeAfters.vue';
export default {
  components: { Landing, Animatable, Introduction, CheckMarks, ShortDescription, Description, ReachUs, QandA, BeforeAfters },
  data() {
    return {
      before_afters: [
        {
          before: {
            image: "/before.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          },
          after: {
            image: "/after.jpeg",
            content: "This patient presented with previous veneers and crowns on her front teeth, multiple cracked teeth and a concern about the color and health of her smile."
          }
        }
      ]
    }
  }
}
</script>

<template>
  <Animatable>
    <Landing image="/woman-with-perfect-smile-whitening-teeth-veneers-v-2LCEPRP.webp" title="GÜLÜŞ TASARIMI" />
    <Introduction heading="Gerçek gülüşünü ortaya çıkar" content="Gülüş tasarımı denilince akla ilk yaprak porselen dişler gelse de, çoğu durumlarda
                yalnızca diş eti estetiği, dudak estetiği, diş temizliği ve diş beyazlatması, ve dişlerdeki çapraşıklıkların
                düzenlenmesi için ortodontik tedavilerle istenilen gülüş yakalanabilir."
      image="/smile-design-landing.jpg" />
    <Description image="/attractive-african-woman-with-perfect-skin-smiling-E4ENK2Q.webp" :left="false"
      heading="Gülüş Tasarımı nedir?"
      :content="[
      {list:false, texts:['Her hastanın estetik gereksinimleri farklı olacağından uygulanacak işlemler kişiye özel olarak planlanır. Bu işlemler belirlenirken hastanın; yüz hatları, cinsiyeti, yaşı ve beklentileri gibi faktörler dikkate alınır. Gülüş tasarımı bu bütünü tamamlayan ve hastaya istediği estetik görünümü ve fonksiyonu kazandırmayı amaçlayan tasarım olarak ifade edilebilir. Bu da çeşitli nedenlerle estetik açıdan görünümü bozulan dişler ve diş etlerinin doğal ve güzel bir görünüme kavuşmasını sağlayarak gerçekleştirilir.', 'Yapılan gülüş dizaynı sonucunda, dişler (Beyaz Estetik) ve diş etlerinde (Pembe Estetik) uygun olan değişikliklerin, hangi miktarda ve nasıl yapılması gerektiği saptanır ve bu planlama sonucu estetik diş hekimliği uygulamalarına geçilir.']}]" />
    <Description image="/dentist-table.jpg" :left="true" heading="Gülüş Tasarımı nasıl yapılır?" :content="[
            {list:false, texts:['Hastanın beklentilerini doğru şekilde analiz edip biyolojiye en uygun şekilde tedavi planını hazırlamak çok önemlidir. İlk seansta hasta ağzından ölçü alınarak model elde edilir.Bu modeller üzerinde planlamalar yapılır. Alınan ağız içi ve yüz fotoğrafları bilgisayar ortamında programlar kullanarak birleştirilir. Hastamıza özel hazırlanan mockup ile geçici restorasyon dişler ağıza uygulanır. Böylece yapılacak tedavinin bitimine yakın bir sonuç görülmüş olur. ']},
        {list:true, texts:['Öncelikle diş etlerinin seviyeleri eşitlenir.', 'Diş eksiklikleri için implant tedavileri ya da diğer tedaviler planlanır.', 'Rengi çok koyu dişlere diş beyazlatma tedavileri uygulanabilir.', 'Bazı diş arası boşluklarda bonding uygulaması dediğimiz estetik dolgular tercih edebilir.', 'Tüm bu seçeneklerin yeterli gelmediği durumlarda yaprak porselen dişlerle dişler restore edilir.']}
    ]" />
    <ShortDescription
      content="Yapılan gülüş dizaynı sonucunda, dişler (Beyaz Estetik) ve diş etlerinde (Pembe Estetik) uygun olan değişikliklerin, hangi miktarda ve nasıl yapılması gerektiği saptanır ve bu planlama sonucu estetik diş hekimliği uygulamalarına geçilir."
      heading="Gülüş Tasarımı" />
    <BeforeAfters :before_afters="before_afters" />
    <ReachUs />
  </Animatable>
</template>
