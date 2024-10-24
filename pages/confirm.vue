<template>
    <div>

        <h1 class="text-5xl font-extrabold dark:text-white">Plese check your Email to confirm registration</h1>

    </div>
</template>

<script setup>
    definePageMeta({
        middleware: [
            async (to, from) => {
                if(from.name !==  'register') return await navigateTo('/')
            }
        ]
    })
</script>
