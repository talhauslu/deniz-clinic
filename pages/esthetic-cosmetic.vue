<script>
import EachService from '../components/sections/services/EachService.vue';
import Animatable from '../components/animation/animatable.vue';
import Landing from '../components/sections/services/Landing.vue';
import Introduction from '../components/sections/services/Introduction.vue';
import Description from '../components/sections/services/Description.vue';
import ReachUs from '../components/ReachUs.vue';
export default {
    components: { EachService, Animatable, Landing, Description, Introduction, ReachUs }
}
</script>

<template>
    <Animatable>
        <Landing image="/aesthetic-landing.webp" title="ESTETİK & KOZMETİK DİŞ HEKİMLİĞİ" />

        <Introduction heading="Modern problemler, modern çözümler."
            content="Ağız bakımı denilince temel problemlerimiz olan diş ağrısı, ağız kokusu ve diş kayıpları gibi sorunlar gelse de günümüzde diş ve diş etlerine bağlı gülüş estetiği çok önemli bir role sahiptir. Kanayan diş etlerin, çapraşık, anormal renkli dişlerin ya da diş kayıplarının sonucunda oluşan estetik sorunlar kişilerde özgüven problemlerine neden olabilir. Teknolojinin ve bilimsel çalışmaların ilerlemesiyle beraber artık pek çok yöntemle daha güzel gülüşler sağlanabilmekte. İşte bu noktada estetik diş hekimliği kavramı hayatımızda daha çok yer edinmektedir."
            image="/aesthetic-cosmetic-introduction.jpg" />
        <h1 class="w-full text-center p-8 text-4xl font-semibold bg-gray-50">Servislerimizi keşfedin</h1>
        <div class="flex flex-row flex-wrap p-8 gap-16 justify-around bg-gray-50">
            <EachService header="Gülüş Tasarımı"
                image_uri="/woman-with-perfect-smile-whitening-teeth-veneers-v-2LCEPRP.webp" />
            <EachService header="Porselen Lamina"
                image_uri="/whitening-concept-dental-care-implants-veneers-wom-AZ5LGPE.webp" />
            <EachService header="Diş Eti Estetiği" image_uri="/gum-esthetic-landing.jpg" />
            <EachService header="Zirkonyum Kaplama" image_uri="/zirconium-landing.jpg" />
            <EachService header="İnlay & Onlay" image_uri="/dentist-taking-dental-filling-from-spatula-to-carver.webp" />
            <EachService header="Diş Beyazlatma" image_uri="/white-teeth.jpg" />
        </div>
        <ReachUs/>
    </Animatable>
</template>