<script>
import AppointmentButton from '../../AppointmentButton.vue';
export default {
    components: { AppointmentButton },
    props:{
        heading:{type:String, required:true, default:""},
        content:{type:String, required:true, default:""},
        image:{type:String, required:true, default:""},
    }
}
</script>

<template>
    <section class="flex flex-col-reverse md:flex-row p-4 justify-around gap-8 md:gap-0 bg-gray-100 z-10">
        <div class="flex flex-col justify-evenly gap-8 md:gap-0 w-full md:w-1/2">

            <h1 class="text-4xl font-semibold text-gray-800">{{heading}}</h1>
            <!-- <i class="fa-regular fa-gem text-6xl text-pink-300 self-center"></i> -->
            <p class="text-xl">{{content}}</p>
            <AppointmentButton />
        </div>
        <nuxt-img class="w-2/3 md:w-1/3 rounded self-center" :src="image" />
    </section>
</template>