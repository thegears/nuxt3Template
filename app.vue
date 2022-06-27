<template>
    <Html>

    <Body>
        <NuxtLayout>
            <NuxtPage />
        </NuxtLayout>
    </Body>

    </Html>
</template>
<script setup>
import { useTheme } from 'vuetify';
const theme = useTheme();

onMounted(() => {
    let lstheme = localStorage.getItem("theme");
    if (lstheme) {
        if (lstheme == "dark") theme.global.name.value = "dark";
        else theme.global.name.value = "light";
    } else localStorage.setItem("theme", "light");
});
</script>