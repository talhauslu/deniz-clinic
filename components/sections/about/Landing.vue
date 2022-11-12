<script>
import AppointmentButton from '../../AppointmentButton.vue';
export default{
    components:{
    AppointmentButton
}
}
</script>

<template>
    <section class="w-full h-90vh relative">
        <nuxt-img class="w-full h-full object-cover absolute" src="/services_background.webp" />
        <div
            class="animation-element fade-up  w-full h-full flex flex-col justify-center items-center relative text-white bg-black bg-opacity-60">
        <div class=" w-4/5 gap-8 md:gap-16 flex flex-col justify-around">
            <h1 class="text-4xl md:text-5xl font-semibold">Profesyonel ekip, sağlıklı iletişim</h1>
            <span class="text-2xl">Hastalarımızın gülüşlerinde farklılıklar yaratırken unutulmaz anılar biriktirmeyi ihmal etmiyoruz.
            </span>
            <AppointmentButton/>
        </div>
        </div>
    </section>
</template>