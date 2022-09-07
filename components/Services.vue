<script>
export default {
    data() {
        return ({
            services: [
                { icon: "fa-solid fa-tooth", header: "DENTAL IMPLANTS", link: "" },
                { icon: "fa-solid fa-tooth", header: "CROWNS", link: "" },
                { icon: "fa-solid fa-tooth", header: "INVISALIGN", link: "" },
                { icon: "fa-solid fa-tooth", header: "GUM TREATMENT", link: "" },
                { icon: "fa-solid fa-tooth", header: "RESTORATIONS", link: "" },
                { icon: "fa-solid fa-tooth", header: "DENTAL CARES", link: "" },
                { icon: "fa-solid fa-tooth", header: "CAD/CAM", link: "" },
                { icon: "fa-solid fa-tooth", header: "ALIGN", link: "" },
                { icon: "fa-solid fa-tooth", header: "VENEERS", link: "" },
            ]
        })
    }
}
</script>

<template>
    <section class="w-full my-4 flex justify-center align-center p-4">
        <div class="w-full md:w-4/5 h-full shadow-md bg-right sm:bg-center" id="services">
            <div class="w-full h-full text-white flex flex-row flex-wrap">
                <div v-for="service in services" class="text-3xl sm:text-5xl h-44 sm:h-52 w-1/2 sm:w-1/3 border bg-black bg-opacity-30 hover:bg-opacity-0 transition-all border-white border-opacity-10 flex flex-col justify-center items-center cursor-pointer">
                    <i :class="service.icon" class="text-xl sm:text-3xl"></i>
                    <h1 class="text-xl select-none">{{service.header}}</h1>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
#services {
    background-image: url(./../static/services_background.webp);
    /* background-position: center; */
    background-repeat: no-repeat;
    background-size: cover;
}
</style>