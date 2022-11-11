<script>
export default{
    props:{
        heading:{type:String, required:false, default:false},
        content:{type:Array, required:false, default:[
            {icon_class:"", subheading:"subheading", content:"content content content content content", border_b:true, border_l:false},
            {icon_class:"", subheading:"subheading", content:"content content content content content", border_b:true, border_l:true},
            {icon_class:"", subheading:"subheading", content:"content content content content content", border_b:false, border_l:false},
            {icon_class:"", subheading:"subheading", content:"content content content content content", border_b:false, border_l:true },
        ]}
    }
}
</script>

<template>
    <section class="p-8 flex flex-col gap-8 items-center">
        <div v-if="heading">
            <h1 class="text-center text-5xl mb-4">{{heading}}</h1>
            <div class="h-0.5 bg-pink-300 w-full"></div>
        </div>
        <div class="flex flex-row flex-wrap justify-around">
            <div v-for="(item, index) of content" :key="item.subheading" class="flex flex-col items-center text-center w-full md:w-1/2 p-2 md:p-8 gap-4" :class="{'md:border-l-2':[1,3].includes(index), 'md:border-b-2':[0,1].includes(index)}">
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