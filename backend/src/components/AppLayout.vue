<template>

    <div class="min-h-full flex bg-gray-200">
        <!-- SIDEBAR-->
        <Sidebar :class="{'-ml-[250px]' : !sidebarOpened}"></Sidebar>
        <!---class="-ml-[250px]"-->
        <!-- SIDEBAR-->
        <div class="flex-1">
            <TopHeader @toggle-sidebar="toggleSidebar"></TopHeader>
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
import {ref, onMounted, onUnmounted} from "vue";

const {title} = defineProps({
    title : String
})

const sidebarOpened = ref(true);

function toggleSidebar(){
    console.log('toogleSidebar');
    sidebarOpened.value = !sidebarOpened.value
}

onMounted(()=> {
    handleSidebarOpened()
    window.addEventListener('resize', handleSidebarOpened)
})

onUnmounted(() => {
    window.removeEventListener('resize', handleSidebarOpened)
})

function handleSidebarOpened(){
    sidebarOpened.value = window.outerWidth > 768;
}
</script>

<style scoped>

</style>
