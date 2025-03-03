<template>
    <figure class="pt-6 text-center space-y-4">
        <img class="w-32 h-32 rounded-full mx-auto" 
            :src=photo 
            alt="profile picture" 
            width="400"
        height="400" />
        <figcaption class="font-medium">
            <div class="text-cyan-900 text-xl ">{{title}}</div>
            <div class="text-gray-500 font-light">{{subtitle}}</div>
        </figcaption>
        <blockquote>
            <p class="text-lg font-medium ">{{headline}}</p>
        </blockquote>
    </figure>
</template>

<script setup>
    const { title, subtitle, headline } = defineProps(['photo','title','subtitle', 'headline']);
</script>
