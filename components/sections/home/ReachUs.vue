<script>
    import ReachUsForm from '../../ReachUsForm.vue';
    export default{
        components:{
            ReachUsForm
        }
    }
</script>

<template>
    <section class="bg-texture w-4/5 flex flex-col md:flex-row justify-center p-4 bg-white">
        <div class="animation-element fade-left w-full md:w-1/2 flex items-center justify-center ">
            <ReachUsForm class="w-full md:w-4/5 h-full"/>
        </div>
        <div  class="animation-element fade-right flex items-center justify-center w-full md:w-2/5">
            <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3007.6627497029776!2d29.025008315376386!3d41.07636397929391!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14cab7b4431dcb6d%3A0xc3a5f8c70b1509d3!2sUzm.%20Dr.%20Deniz%20Y%C4%B1lmaz!5e0!3m2!1sen!2str!4v1662646830852!5m2!1sen!2str"
                class="w-full h-30vw left-0 right-0" style="border:0;" allowfullscreen="" loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
    </section>
</template>
