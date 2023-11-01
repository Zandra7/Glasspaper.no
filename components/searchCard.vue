<template>
    <div class="kurs-sertif-bg">
        <div class="kurs-sertif-content">
            <h1>Kurs og sertifisering</h1>
            <p class="kurs-sertif-text">Vi har en rekke kurs og sertifiseringer, <label class="text-link">se full liste her</label></p>
            <p>Eller bruk søkefeltet under</p>
            <div class="relative">
                <input type="text" placeholder="Søk i kurs og sertifisering">
                <img src="~/public/images/searchIcon.png" alt="Search Icon" class="search-icon">
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
    .kurs-sertif-bg {
        display: flex;
        flex-direction: column;
        margin: 2rem auto;
        max-width: 1170px;
        height: 240px;
        background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 1)), url('~/public/images/img1.png');
        background-size: cover;
    }

    .kurs-sertif-content {
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        height: 100%;
        padding: 0 8rem;
    }

    h1 {
        font-size: 36px;
        padding-top: 1.25rem;
        padding-bottom: 0.75rem;
    }

    .kurs-sertif-text {
        margin-bottom: 0.25rem;
    }

    .text-link {
        font-weight: bold; 
        cursor: pointer;
    }
    .text-link:hover {
        text-decoration: underline;
        text-underline-offset: 2px;
    }

    input {
        padding: 0.75rem 2.5rem;
        margin: 1.5rem 0;
        width: 100%;
        height: 3rem;
        color: black;
        border-radius: 0.25rem;
        font-size: 1rem;
        font-weight: 300;
        text-align: center;
        font-weight: 200;
    }
    ::placeholder {
        color: black;
        font-weight: 200;
        font-size: 1.125rem;
    }

    .search-icon {
        position: absolute;
        right: 1rem;
        top: 50%;
        cursor: pointer;
        transform: translateY(-50%);
        width: 1.25rem;
    }

    @media (max-width: 640px) {
        .kurs-sertif-bg {
            padding: 0 2rem;
        }

        h1 {
            font-size: 24px;
            padding-top: 1rem;
            padding-bottom: 0.5rem;
        }

        .kurs-sertif-content {
            padding: 0;
        }

        .kurs-sertif-text {
            margin-bottom: 1rem;
        }
    }

    @media (min-width: 1024px) {
        h1 {
            padding-top: 1rem;
            padding-bottom: 1rem;
        }

        .kurs-sertif-text {
            margin-bottom: 0.5rem;
        }
    }
</style>
