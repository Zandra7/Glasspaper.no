<template>
    <div class="kurs-sertif-bg flex flex-col mx-auto mt-8 sm:mt-10 lg:mt-12">
        <div class="kurs-sertif-content px-4 sm:px-8 md:px-16 lg:px-32 text-white">
            <h1 class="text-3xl sm:text-4xl pt-5 sm:pt-8 lg:pt-10 pb-3 sm:pb-4 lg:pb-7">Kurs og sertifisering</h1>
            <p class="mb-1 sm:mb-1.5 lg:mb-2.5">Vi har en rekke kurs og sertifiseringer, <label class="font-bold cursor-pointer hover:underline hover:underline-offset-2">se full liste her</label></p>
            <p>Eller bruk søkefeltet under</p>
            <div class="relative">
                <input type="text" class="pl-10 sm:pl-12 lg:pl-16 w-full py-3 sm:py-4 px-6 sm:px-7 lg:px-8 text-center rounded-sm my-6 sm:my-8 lg:my-12 text-center border text-black font-extralight text-xl sm:text-2xl placeholder:text-black placeholder:font-extralight placeholder:text-xl sm:placeholder:text-2xl" placeholder="Søk i kurs og sertifisering">
                <img src="~/public/images/searchIcon.png" alt="Search Icon" class="absolute right-3 sm:right-4 lg:right-5 top-1/2 transform -translate-y-1/2 w-5 sm:w-6 h-5 sm:h-6 cursor-pointer">
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
    .kurs-sertif-bg {
        max-width: 1170px;
        height: 240px;
        background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 1)), url('~/public/images/img1.png');
        background-size: cover;

        /* Responsive Height */
        @media (min-width: 640px) { /* sm: */
            height: 280px;
        }

        @media (min-width: 1024px) { /* lg: */
            height: 320px;
        }
    }
</style>
