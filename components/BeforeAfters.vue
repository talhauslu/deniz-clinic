<script>
import BeforeAfter from './BeforeAfter.vue';
export default {
  components: {
    BeforeAfter
  },
  props: {
    before_afters: {
      type: Array,
      required: true,
    }
  },
  data() {
    return {
      before: false,
      after: false
    }
  }
}
</script>

<template>
  <section class="flex flex-col p-4 items-center text-center w-full gap-8">
    <div class="w-full md:w-auto">
      <h1 class="text-4xl font-light px-8 text-gray-900">Önce & Sonra</h1>
      <div class="h-px w-full bg-gray-500"></div>
    </div>
    <BeforeAfter v-for="before_after in before_afters" :before_after="before_after" :key="before_after.before.image"/>
  </section>
</template>
