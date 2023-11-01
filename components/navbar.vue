<template>
    <nav class="navbar text-white">
        <div class="content flex flex-col mx-auto">
            <div class="flex gap-2 justify-end pt-3">
                <p>EN</p>
                <p>|</p>
                <p>NO</p>
            </div>
            <img src="~/public/images/logo.svg" alt="Glasspaper logo" class="w-64">
            <div class="pb-3 flex flex-row gap-12 justify-end">
                <p class="cursor-pointer hover:underline hover:decoration-orange-500 hover:underline-offset-4">Tjenester</p>
                <p class="cursor-pointer hover:underline hover:decoration-orange-500 hover:underline-offset-4">Om oss</p>
                <p class="cursor-pointer hover:underline hover:decoration-orange-500 hover:underline-offset-4">Kontakt oss</p>
                <p class="cursor-pointer hover:underline hover:decoration-orange-500 hover:underline-offset-4">Ledige stillinger</p>
            </div>
        </div>
    </nav>
</template>

<script setup>

</script>

<style scoped>
    .navbar {
        background-color: rgba(88, 110, 114, 1);
    }
    .content {
        max-width: 1170px;
        
        @media screen and (max-width: 1175px) {
            padding: 0 2rem;
        }
    }
</style>