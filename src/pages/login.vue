<script setup>
import UndrawLogin from "vue-undraw/UndrawLogin.vue"
</script>

<template>
<div class="flex flex-col items-center justify-center space-y-12 min-h-screen-nonav">
    <div class="flex items-center justify-center overflow-hidden bg-green-100 rounded-lg shadow-2xl">
        
        <UndrawLogin primary-color='#41B883' class="h-64 bg-white" />
        <form class="flex flex-col p-4 space-y-4">
            <input type="text" class="p-2 border-2 rounded-lg"
              placeholder="Username" v-model="username" />
              <input type="password" class="p-2 border-2 rounded-lg"
              placeholder="Password" v-model="password" />
              <button type="submit" class="py-2 text-green-200 bg-green-600 rounded-lg">Login</button>
        </form>
    </div>
</div>
    
</template>