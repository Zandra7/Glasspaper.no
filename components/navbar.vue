<template>
    <nav class="navbar">
        <div class="content">
            <div class="lang">
                <p>EN</p>
                <p>|</p>
                <p>NO</p>
            </div>
            <div class="logo-burger">
                <img src="~/public/images/logo.svg" alt="Glasspaper logo" class="gp-logo">
                <svg @click="isOpen = !isOpen" viewBox="0 0 20 20" fill="currentColor" class="hamburger"><path fill-rule="evenodd" d="M4 5a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zm0 6a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zm1 5a1 1 0 100 2h10a1 1 0 100-2H5z" clip-rule="evenodd"></path></svg>
            </div>
            <div class="nav-items" :class="{'nav-items-vertical': isOpen}">
                <p class="nav-item">Tjenester</p>
                <p class="nav-item">Om oss</p>
                <p class="nav-item">Kontakt oss</p>
                <p class="nav-item">Ledige stillinger</p>
            </div>
        </div>
    </nav>
</template>

<script setup>
    import { ref } from 'vue'
    const isOpen = ref(false)
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

    .logo-burger {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
    }

    .hamburger {
        display: none;
    }

    @media (max-width: 1175px) {
        .content {
            padding: 0 2rem;
        }
    }

    @media (max-width: 768px) {
        .content {
            padding: 0 1rem;
        }
        .lang {
            display: none;
        }

        .nav-items {
            display: none;
        }

        .nav-items-vertical {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: start;
            position: fixed;
            top: 3.5rem;
            right: 0;
            height: 100%;
            background-color: rgba(88, 110, 114, 1);
            z-index: 10000;
        }
        .hamburger {
            display: inline-block;
            width: 1.5rem;
            padding: 1.25rem 0;
        }

        .nav-items, .lang {
            padding: 1rem 1rem;
        }
        .gp-logo {
            width: 12rem;
            padding: 1rem 0;
        }
    }

</style>