<script>
import TypeWriter from './../../TypeWriter.vue'
export default {
    components:{
        TypeWriter
    }
}
</script>

<template>

    <section class="animation-element w-full flex flex-col items-center justify-around md:flex-row bg-shift-wb text-white md:h-90vh gap-4 md:gap-0 p-8 md:p-0 relative">
        <nuxt-img class="animation-element fade-left object-cover w-4/5 md:w-1/2 shadow-lg" src="/veneers.png" />
        <div class="animation-element fade-right w-full md:w-1/2 flex flex-col gap-4 md:gap-12 justify-around md:p-8">
            <h1 class="text-6xl">{{$t('index').shortdescription_veneers.heading}}</h1>
            <h2 class="text-4xl flex flex-col sm:flex-row gap-1 text-gray-400">
                <span>{{$t('index').shortdescription_veneers.more}}</span> <span> </span>
                <TypeWriter class="text-blue-100" :speed="100" :delay="500"
                    :words="$t('index').shortdescription_veneers.typewriter_keys" />
            </h2>
            <span>{{$t('index').shortdescription_veneers.content}}</span>
            <NuxtLink to="/porcelain-laminate"
                class="inline self-start p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all  shadow-md">
                {{$t('basics').read_more}}
            </NuxtLink>
        </div>
        <nuxt-img class="hidden md:block absolute right-0 top-0" src="/dots-corner.png"></nuxt-img>
    </section>

</template>
