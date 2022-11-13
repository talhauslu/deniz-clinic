<script>
export default {
}
</script>

<template>
    <section class="w-full my-4 flex flex-col justify-center items-center text-center py-3 gap-8">
        <div>
            <h1 class="text-5xl text-gray-800 font-light">{{$t('index').services.heading}}</h1>
            <div class="w-full h-0.5 bg-gray-800 mt-2 shadow"></div>
        </div>
        <div  class="w-full md:w-4/5 h-full shadow-md bg-right sm:bg-center bg-blue-300" id="services">
            <div class="animation-element fade-up w-full h-full text-white flex flex-row flex-wrap">
                <NuxtLink v-for="service in $t('index').services.services" :to="localePath(service.link)" :key="service.header"
                    class="text-3xl sm:text-5xl h-44 sm:h-52 w-1/2 sm:w-1/3 border bg-black bg-opacity-50 hover:bg-opacity-0 transition-all border-white border-opacity-10 flex flex-col justify-center items-center cursor-pointer">
                    <i :class="service.icon" class="text-xl sm:text-3xl"></i>
                    <h1 class="text-xl select-none">{{service.header}}</h1>
                </NuxtLink>
            </div>
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #ffffff;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='199' viewBox='0 0 100 199'%3E%3Cg fill='%23eff6ff' fill-opacity='1'%3E%3Cpath d='M0 199V0h1v1.99L100 199h-1.12L1 4.22V199H0zM100 2h-.12l-1-2H100v2z'%3E%3C/path%3E%3C/g%3E%3C/svg%3E");
}

#services {
    background-image: url(./../../../static/services_background.webp);
    /* background-position: center; */
    background-repeat: no-repeat;
    background-size: cover;
}
</style>
