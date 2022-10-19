<script>
export default{
    props:{
        heading:{type:String, required:false, default:"Heading"},
        content:{type:Array, required:false, default:[
            {icon_class:"", subheading:"subheading", content:"content content content content content"},
            {icon_class:"", subheading:"subheading", content:"content content content content content"},
            {icon_class:"", subheading:"subheading", content:"content content content content content"},
            {icon_class:"", subheading:"subheading", content:"content content content content content"},
        ]}
    }
}
</script>

<template>
    <section class="bg-blue-50 p-8 flex flex-col gap-8 items-center">
        <!-- <div>
            <h1 class="text-center text-5xl mb-4">{{heading}}</h1>
            <div class="h-0.5 bg-pink-300 w-full"></div>
        </div> -->
        <div class="flex flex-row flex-wrap justify-around">
            <div v-for="item of content" class="flex flex-col items-center text-center w-full md:w-1/2 p-2 md:p-8 gap-4">
                <i class="fa-solid fa-check text-4xl text-pink-400"></i>
                <h1 class=" text-3xl">
                    {{item.subheading}}
                </h1>
                <span>
                    {{item.content}}
                </span>
            </div>
        </div>
    </section>
</template>