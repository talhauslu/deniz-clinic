<script>
export default {
    props: {
        qas: {
            type: Array, required: true, default: [
                { q: "question1", a: "answer1", visible: false },
                { q: "question2", a: "answer2", visible: false },
                { q: "question3", a: "answer3", visible: false },
                { q: "question4", a: "answer4", visible: false },
            ]
        }
    },
    data(){
        return{
            local_qas : null
        }
    },
    mounted(){
        this.local_qas = this.qas
    },
    methods: {
        toggleQA(question = "") {
            this.local_qas.map(qa => {
                if (qa.q === question) {
                    qa.visible = !qa.visible
                    return qa
                }
            })
        }
    }
}
</script>

<template>
    <section class="flex flex-col bg-gray-50 rounded border w-full  md:w-4/5 self-center shadow m-4 p-8 cursor-pointer">
        <h1 class="text-3xl text-center mb-4">Sık sorulan sorular</h1>
        <div v-for="qa in local_qas" @click="toggleQA(qa.q)" :key="qa.q" class="flex flex-col gap-4 border-b p-8">
            <h1 class="text-xl font-semibold flex flex-row w-full justify-between">
                <span>{{qa.q}}</span> <i class="fa-solid"
                    :class="{'fa-chevron-up':qa.visible, 'fa-chevron-down':!qa.visible}"></i>
            </h1>
            <Transition  name="fade">
                <span v-if="qa.visible">
                   > {{qa.a}}
                </span>
            </Transition>
        </div>
    </section>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
}
</style>