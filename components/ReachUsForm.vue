<template>
    <form class="animation-element fade-left flex flex-col justify-around gap-4 p-4 text-gray-700">
        <h1 class="text-2xl font-semibold">{{$t('reach_us').heading}}</h1>

        <div class="w-full flex flex-row justify-between">
            <label>{{$t('reach_us').name}}:</label>
            <input name="name" type="text" class="w-4/5" />
        </div>
        <div class="w-full flex flex-row justify-between">
            <label>{{$t('reach_us').email}}:</label>
            <input name="email" type="email" class="w-4/5" />
        </div>
        <div class="w-full flex flex-row justify-between">
            <label>{{$t('reach_us').message}}:</label>
            <textarea name="message" rows="4" class="w-4/5 resize-none" />
        </div>

        <div>
            <button type="submit"
                class="bg-pink-400 border hover:bg-pink-500 transition-all p-2 text-sm float-right rounded text-white">{{$t('reach_us').send}}</button>
        </div>

    </form>
</template>
