<script setup>
import { auth } from "../firebase.js"
import { useAuth } from "@/composables/useAuth.js";

const { user, logout } = useAuth()

</script>



<template>
    <h1>Soy Dashboard</h1>
    <h2 v-if="user">Bienvenido, {{ user.displayName }} </h2>
    <button @click="logout">Logout</button>

</template>