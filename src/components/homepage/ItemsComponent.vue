<script setup>
    import { ref } from 'vue';
    import ItemsCardComponent from '../ItemsCardComponent.vue';

    const items = ref([
        {id: 1, title: "Mobile UI Kit", category: "Mobile UI Kit", image: "items-1.jpg"},
        {id: 1, title: "Online Doctor Consultation", category: "Website UI Kit", image: "items-2.jpg"},
        {id: 1, title: "Banking Crypto", category: "Mobile UI Kit", image: "items-3.jpg"},
    ]);
</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12">
      <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">New Items</h2>
      <div class="flex flex-wrap -mx-1 lg:-mx-4">
        <ItemsCardComponent v-for="item in items" :key="item.id" :title="item.title" :category="item.category" :image="item.image"/>
      </div>
    </div>
</template>