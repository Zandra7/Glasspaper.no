<template>
    <nav class="navbar">
        <div class="content">
            <div class="lang">
                <p>EN</p>
                <p>|</p>
                <p>NO</p>
            </div>
            <img src="~/public/images/logo.svg" alt="Glasspaper logo" class="gp-logo">
            <div class="nav-items">
                <p class="nav-item">Tjenester</p>
                <p class="nav-item">Om oss</p>
                <p class="nav-item">Kontakt oss</p>
                <p class="nav-item">Ledige stillinger</p>
            </div>
        </div>
    </nav>
</template>

<script setup>

</script>

<style scoped>
    .navbar {
        background-color: rgba(88, 110, 114, 1);
        color: white;
    }
    .content {
        display: flex;
        flex-direction: column;
        margin: 0 auto;
        max-width: 1170px;
        
        @media screen and (max-width: 1175px) {
            padding: 0 2rem;
        }
    }
    .lang {
        display: flex;
        flex-direction: row;
        justify-content: end;
        gap: 0.5rem;
        padding-top: 1rem;
    }
    .gp-logo {
        width: 16rem;
    }
    .nav-items {
        display: flex;
        flex-direction: row;
        justify-content: end;
        gap: 3rem;
        padding-bottom: 1rem;
    }
    .nav-item {
        cursor: pointer;
    }
    .nav-item:hover {
        text-decoration: underline;
        text-underline-offset: 4px;
        text-decoration-color: #c44111;
    }
</style>