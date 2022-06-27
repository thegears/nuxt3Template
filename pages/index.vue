<template>
    <div class="w-full flex justify-center h-screen items-center">
        <vBtn @click="changeTheme">Change Theme</vBtn>
    </div>
</template>
<script setup>
import { useTheme } from 'vuetify';
const theme = useTheme();

function changeTheme() {
    if (theme.global.current.value.dark) {
        theme.global.name.value = "light";
        localStorage.setItem("theme","light");
    } else {
        theme.global.name.value = "dark";
        localStorage.setItem("theme","dark");
    };
};
</script>