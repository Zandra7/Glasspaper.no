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
                <p class="cursor-pointer">Tjenester</p>
                <p class="cursor-pointer">Om oss</p>
                <p class="cursor-pointer">Kontakt oss</p>
                <p class="cursor-pointer">Ledige stillinger</p>
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
    }
</style>