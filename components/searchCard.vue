<template>
        <div class="kurs-sertif-bg flex flex-col">
            <div class="kurs-sertif-content mx-32 text-white">
                <h1 class="text-4xl pt-10 pb-7">Kurs og sertifisering</h1>
                <p class="mb-2.5">Vi har en rekke kurs og sertifiseringer, <label class="font-bold underline underline-offset-2">se full liste her</label></p>
                <p>Eller bruk søkefeltet under</p>
                <div class="relative">
                    <input type="text" class="pl-16 w-full py-4 px-8 text-center rounded-sm my-12 placeholder:text-black placeholder:font-extralight placeholder:text-2xl text-center border" placeholder="Søk i kurs og sertifisering">
                    <img src="~/public/images/searchIcon.png" alt="Search Icon" class="absolute right-4 top-1/2 transform -translate-y-1/2 w-6 h-6">
                </div>
            </div>
        </div>
</template>

<script setup>
</script>

<style scoped>
    .kurs-sertif-bg {
        width: 1170px;
        height: 320px;
        margin: 0 auto;
        background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 1)), url('~/public/images/img1.png');
        background-size: cover;
        margin-top: 2rem;
    }
</style>