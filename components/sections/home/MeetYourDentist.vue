<template>
    <section class="flex flex-col md:flex-row bg-white p-8 gap-4 md:gap-0">
        <div class="animation-element fade-left w-full md:w-1/2 flex justify-center items-center">
            <nuxt-img class="w-3/4 object-contain shadow-xl" src="/deniz1.png" />
        </div>
        <div class="animation-element fade-right w-full md:w-2/3 flex flex-col justify-center gap-8 text-center md:text-left">
            <h1 class="text-4xl font-semibold text-gray-700">Uzm. Dr. Deniz Yılmaz ile tanış</h1>
            <span>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur aliquam autem fugiat. Similique
                debitis praesentium reiciendis quae. Neque earum atque et, distinctio soluta eius consequatur fugit?
                Dignissimos expedita id dolorum.
            </span>
            <NuxtLink to="/about"
                class="inline self-start p-4 rounded-lg bg-gray-600 font-semibold border text-white hover:bg-opacity-50 transition-all shadow-md">
                Daha fazlası
            </NuxtLink>
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #ffffff;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='199' viewBox='0 0 100 199'%3E%3Cg fill='%23eff6ff' fill-opacity='1'%3E%3Cpath d='M0 199V0h1v1.99L100 199h-1.12L1 4.22V199H0zM100 2h-.12l-1-2H100v2z'%3E%3C/path%3E%3C/g%3E%3C/svg%3E");
}
</style>