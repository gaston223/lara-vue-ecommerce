<template>

    <div class="min-h-full flex bg-gray-200">
        <!-- SIDEBAR-->
        <Sidebar></Sidebar>
        <!-- SIDEBAR-->
        <div class="flex-1">
            <TopHeader></TopHeader>
            <!-- CONTENT-->
            <main class="p-6">
                <router-view></router-view>
            </main>
        </div>
    </div>

</template>

<script setup>
import Sidebar from "./Sidebar.vue";
import TopHeader from "./TopHeader.vue";

const {title} = defineProps({
    title : String
})

const emit = defineEmits(['submit'])
</script>

<style scoped>

</style>
