<template>
    <div class="kurs-sertif-bg">
        <div class="kurs-sertif-content">
            <h1>Kurs og sertifisering</h1>
            <p class="kurs-sertif-text">Vi har en rekke kurs og sertifiseringer, <label class="text-link">se full liste her</label></p>
            <p>Eller bruk søkefeltet under</p>
            <div>
                <label class="relative">
                    <input type="text" placeholder="Søk i kurs og sertifisering">
                    <img src="~/public/images/searchIcon.png" alt="Search Icon" class="search-icon">
                </label>
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
        margin: 13.69rem auto 2rem auto;
        max-width: 1170px;
        background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 1)), url('~/public/images/img1.png');
        background-size: cover;
    }
    .kurs-sertif-content {
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 0 8rem;
    }

    h1 {
        font-weight: 500;
        font-size: 2.25rem;
        padding-top: 2.63rem;
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
        margin: 1.5rem 0 3rem 0;
        width: 100%;
        height: 2.5rem;
        color: black;
        border-radius: 0.125rem;
        background: white;
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

    .relative {
        position: relative;
    }
    
    .search-icon {
        cursor: pointer;
        transform: translateY(-50%);
        width: 1.25rem;
        position: absolute;
        top: 50%;
        right: 1.5rem;
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

    @media (max-width: 768px) {
        .kurs-sertif-bg {
            margin: 5.69rem auto 2rem auto;
        }
    }

    @media (min-width: 1024px) {
        h1 {
            padding-top: 1rem;
        }
    }
</style>
