<script setup>
import {ref} from "vue";
import {useRouter} from "vue-router";
import UndrawLogin from "vue-undraw/UndrawLogin.vue";
import useAuth from "../composable/useAuth";

const {isAuthenticated, login} = useAuth();

const username = ref("");
const password = ref("");

const router = useRouter();

const logginIn = () => {
    login(username.value,  password.value);
    if(isAuthenticated.value) {
        router.push("/");
    } else {
        alert(5);
    }
};


</script>

<template>
<div class="flex flex-col items-center justify-center space-y-12 min-h-screen-nonav">
    <div class="flex items-center justify-center overflow-hidden bg-green-100 rounded-lg shadow-2xl">
        
        <UndrawLogin primary-color='#41B883' class="h-64 bg-white" />
        <form @submit.prevent="logginIn" class="flex flex-col p-4 space-y-4">
            <input type="text" class="p-2 border-2 rounded-lg"
              placeholder="Username" v-model="username" />
              <input type="password" class="p-2 border-2 rounded-lg"
              placeholder="Password" v-model="password" />
              <button @submit.prevent="logginIn" type="submit" class="py-2 text-green-200 bg-green-600 rounded-lg">Login</button>
        </form>
    </div>
</div>
    
</template>