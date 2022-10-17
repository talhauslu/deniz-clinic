<script>
export default {
    props: {
        heading: { type: String, required: true, default: "Heading" },
        content: { type: String, required: true, default: "Orthodontic treatments like braces and Invisalign create constant pressure on your teeth. This can lead to inflammation, bone loss, and gum recession. Our periodontists have 3 years of specialized training in bone, gum, and supporting tissue. Dr. Pumphrey regularly partners with orthodontists to limit the risk of damage to gums, soft tissue, and bone." }
    }
}
</script>

<template>
    <section class="relative ">
        <div class="animation-element fade-up flex flex-col justify-around gap-6 text-center z-10 relative bg-black bg-opacity-70 w-full h-full py-16 px-4 sm:px-8 md:px-12 lg:px-16 text-white">
            <div class="flex justify-center items-center">
                <i class="fa-solid fa-gem text-6xl sm:text-4xl text-pink-400"></i>
            </div>
            <h1 class="font-semibold">
                {{heading}}
            </h1>
            <span>
                {{content}}
            </span>
        </div>
        <nuxt-img class="absolute w-full h-full top-0 left-0 right-0 bottom-0 object-cover" src="/up-of-dental-treatment-equipment-dentist-dental-ca-DUH3F2R.webp" />
    </section>
</template>