<template>
<div class="text-green-200 bg-green-800">
    <div class= "container flex items-center justify-between mx-auto">
        <h1 class="text-3xl font-thin tracking-tighter">
            Vue<span class="font-normal">FakeAuth</span>
        </h1>
        <nav>
            <ul class="flex space-x-4">
                <router-link to="/">
                <li class="px-4 py-8 hovver:cursor-pointer hover:bg-green-500 hover:text-green-800">Home</li>
                </router-link>
                <router-link :to="{name:'About'}">
                <li class="px-4 py-8 hovver:cursor-pointer hover:bg-green-500 hover:text-green-800">About</li>
                </router-link>
                <router-link :to="{path: '/news', name:'News'}">
                <li class="px-4 py-8 hovver:cursor-pointer hover:bg-green-500 hover:text-green-800">News</li>
                </router-link>
                 <router-link :to="{path: '/contact'}">
                <li class="px-4 py-8 hovver:cursor-pointer hover:bg-green-500 hover:text-green-800">Contact</li>
                </router-link>
                <router-link :to="{path: '/login'}">
                <li class="px-4 py-8 hovver:cursor-pointer hover:bg-green-500 hover:text-green-800">Login</li>
                </router-link>
            </ul>
        </nav>
    </div>
</div>
    
</template>