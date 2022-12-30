<!--<template>
    <div class="w-[200px] bg-indigo-700 text-white py-4 px-2">
        <router-link :to="{name : 'app.dashboard'}" class="flex items-center p-2 rounded transition-colors hover:bg-black/30">
            <span class="mr-2">
                <HomeIcon class="w-4"></HomeIcon>
            </span>
            <span class="text-xs">Tableau de bord</span>
        </router-link>
        <router-link :to="{name : 'app.dashboard'}" class="flex items-center p-2 rounded transition-colors hover:bg-black/30">
            <span class="mr-2">
                <ShoppingCartIcon class="w-4"></ShoppingCartIcon>
            </span>
            <span class="text-xs">Articles</span>
        </router-link>
        <router-link :to="{name : 'app.dashboard'}" class="flex items-center p-2 rounded transition-colors hover:bg-black/30">
            <span class="mr-2">
                <UserIcon class="w-4"></UserIcon>
            </span>
            <span class="text-xs">Utilisateurs</span>
        </router-link>
        <router-link :to="{name : 'app.dashboard'}" class="flex items-center p-2 rounded transition-colors hover:bg-black/30">
            <span class="mr-2">
                <ChartPieIcon class="w-4"></ChartPieIcon>
            </span>
            <span class="text-xs">Statistiques</span>
        </router-link>

    </div>

</template>-->
<template>
    <div
        class="sidebar p-2 w-[250px] transition-all overflow-y-auto text-center bg-gray-900"
    >
        <div class="text-gray-100 text-xl">
            <div class="p-2 mt-1 flex items-center">
                <ShoppingBagIcon class="w-4 rounded-md"></ShoppingBagIcon>
                <h1 class="font-bold text-gray-200 text-[15px] ml-3">LaraVue Ecommerce</h1>

            </div>
            <div class="my-2 bg-gray-600 h-[1px]"></div>
        </div>
        <router-link :to="{name : 'app.dashboard'}"
            class="p-2 mt-3 flex items-center rounded-md px-4 duration-300 cursor-pointer hover:bg-violet-600 text-white"
        >
            <HomeIcon class="w-4"></HomeIcon>
            <span class="text-[15px] ml-4 text-gray-200">Tableau de bord</span>
        </router-link>

        <router-link :to="{name : 'app.products'}"
                     class="p-2 mt-3 flex items-center rounded-md px-4 duration-300 cursor-pointer hover:bg-violet-600 text-white"
        >
            <ShoppingCartIcon class="w-4"></ShoppingCartIcon>
            <span class="text-[15px] ml-4 text-gray-200">Articles</span>
        </router-link>

        <router-link :to="{name : 'app.dashboard'}"
                     class="p-2 mt-3 flex items-center rounded-md px-4 duration-300 cursor-pointer hover:bg-violet-600 text-white"
        >
            <UserIcon class="w-4"></UserIcon>
            <span class="text-[15px] ml-4 text-gray-200">Utilisateurs</span>
        </router-link>

        <router-link :to="{name : 'app.dashboard'}"
                     class="p-2 mt-3 flex items-center rounded-md px-4 duration-300 cursor-pointer hover:bg-violet-600 text-white"
        >
            <ChartPieIcon class="w-4"></ChartPieIcon>
            <span class="text-[15px] ml-4 text-gray-200">Reporting</span>
        </router-link>
    </div>
</template>

<script setup>
//import { HomeIcon, UserIcon, ShoppingCartIcon, ChartPieIcon, ShoppingBagIcon} from '@heroicons/vue/24/outline'
import { HomeIcon, UserIcon, ShoppingCartIcon, ChartPieIcon, ShoppingBagIcon} from '@heroicons/vue/24/solid'

</script>

<style scoped>

</style>
