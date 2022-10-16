<script>
import Landing from '../../components/sections/services/Landing.vue';
import Animatable from '../../components/animation/animatable.vue';
import Introduction from '../../components/sections/services/Introduction.vue';
export default {
    components: { Landing, Animatable, Introduction }
}
</script>

<template>
    <Animatable>
        <Landing image="/whitening-concept-dental-care-implants-veneers-wom-AZ5LGPE.webp"
            title="PORSELEN LAMİNA & LAMINATE VENEERS" />
        <Introduction class="b" heading="Daha doğal, daha beyaz."
            content="Laminate Veneer restorasyonlar, Dişlerin sadece ön yüzeylerinden minimal (0.3-0.7 mm) aşındırmalar yaparak, bazı zamanlar ise hiç aşındırma yapmadan sadece ölçü alınarak bu alanlara çok ince porselen diş laminalarının yapıştırılması işlemidir. Yaprak porselen dişler, estetik, güvenli, diş eti irritasyonu yaratma riski az ve konservatif bir tedavidir. Çok ince olmaları sebebiyle ışığın geçirgenliğine izin verirler. Bu nedenle, dişler doğal görünebilmektedir."
            image="/dental-crown.jpg" />
    </Animatable>
</template>