<script>
export default {
  props: {
    before_after: {
      type: Object,
      required: true
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
  <div class="flex flex-col w-full gap-4 pb-4 border-b md:border-none ">
    <div :key="before_after.before.image" class="flex flex-col md:flex-row justify-center gap-8 w-full text-sm">
      <div @mouseover="before = true" @mouseleave="before = false" class="relative h-40 md:h-56 w-full md:w-1/3">
        <nuxt-img class="absolute w-full h-full object-cover" :src="before_after.before.image" />
        <div :class="{'hidden':!after, 'flex':after}"
          class="z-10 relative w-full h-full bg-gray-300 text-black p-8 flex flex-col justify-around text-right">
          <h1 class="text-base font-semibold">
            <span>Sonra</span>
            <i class="hidden md:inline fa-solid fa-circle-arrow-right"></i>
          </h1>
          <span>{{ before_after.after.content }}</span>
        </div>
      </div>
      <div @mouseover="after = true" @mouseleave="after = false" class="relative h-40 md:h-56 w-full md:w-1/3">
        <nuxt-img class="absolute w-full h-full object-cover" :src="before_after.after.image" />
        <div :class="{'hidden':!before, 'flex':before}"
          class="z-10 relative w-full h-full bg-gray-300 text-black p-8 flex flex-col justify-around text-left">
          <h1 class="text-base font-semibold">
            <i class="hidden md:inline fa-solid fa-circle-arrow-left"></i>
            <span>Önce</span>
          </h1>
          <span>{{ before_after.before.content }}</span>
        </div>
      </div>
    </div>
    <span class="w-full md:w-2/3 text-center self-center text-gray-600" v-if="before_after.description">{{before_after.description}}</span>
  </div>
</template>
