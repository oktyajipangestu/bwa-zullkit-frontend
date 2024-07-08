<script setup>
import { ref } from 'vue';

const defaultImage = ref('gallery-1.png');

const listImages = ref([
    {id: 1, image: 'gallery-1.png'},
    {id: 2, image: 'gallery-2.png'},
    {id: 3, image: 'gallery-3.png'},
    {id: 4, image: 'gallery-4.png'},
]);

function changePhoto(image) {
    this.defaultImage = image
}
</script>

<template>
    <section id="gallery">
        <img :src="'../src/assets/img/' + defaultImage" alt="" class="w-full mt-6 rounded-2xl">
        <div class="grid grid-cols-4 gap-4 mt-4">
            <template v-for="image in listImages" :key="image.id">
                <div class="overflow-hidden cursor-pointer rounded-2xl" @click="changePhoto(image.image)">
                    <img :src="'../src/assets/img/' + image.image" class="w-full" alt="">
                </div>
            </template>
        </div>
    </section>
</template>