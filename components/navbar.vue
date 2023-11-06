<template>
    <nav class="navbar" ref ="navbar">
        <div class="content">
            <div class="lang">
                <p class="lang-option">EN</p>
                <p class="lang-separator">|</p>
                <p class="lang-option">NO</p>
            </div>
            <div class="logo-burger">
                <img src="~/public/images/logo.svg" alt="Glasspaper logo" class="gp-logo">
                <svg @click="isOpen = !isOpen" viewBox="0 0 20 20" fill="currentColor" class="hamburger"><path fill-rule="evenodd" d="M4 5a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zm0 6a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zm1 5a1 1 0 100 2h10a1 1 0 100-2H5z" clip-rule="evenodd"></path></svg>
            </div>
            <div class="nav-items" :class="{'nav-items-vertical': isOpen}">
                    <p class="nav-item">Tjenester</p>
                    <p class="nav-item">Om oss</p>
                    <p class="nav-item">Kontakt oss</p>
                    <p class="nav-item">Ledige stillinger</p> <!-- how can I select this element with css without creating a new class? -->
                <div class="vertical-lang" :class="{'lang-vertical': isOpen}">
                    <p class="lang-option">EN</p>
                    <p class="lang-separator">|</p>
                    <p class="lang-option">NO</p>
                </div>    
            </div>
        </div>
    </nav>
</template>

<script setup>
    import { ref, onMounted, onUnmounted } from 'vue'

    const navbar = ref(null)
    const isOpen = ref(false)

    const handleClickOutside = event => {
        if (navbar.value && !navbar.value.contains(event.target)) {
            isOpen.value = false
        }
    }

    onMounted(() => {
        document.addEventListener('click', handleClickOutside)
    })
    onUnmounted(() => {
        document.removeEventListener('click', handleClickOutside)
    })
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
        justify-content: flex-end;
        gap: 0.5rem;
        padding-top: 1rem;
    }
    .gp-logo {
        width: 16rem;
        cursor: pointer;
    }
    .nav-items {
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        gap: 3rem;
        padding-bottom: 1rem;
    }

    .nav-item:hover, .lang-option:hover {
        cursor: pointer;
        text-decoration: underline;
        text-underline-offset: 4px;
        text-decoration-color: #c44111;
    }
    .lang-separator {
        cursor: default;
    }

    .logo-burger {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
    }

    .hamburger {
        display: none;
        cursor: pointer;
    }

    .vertical-lang {
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

        .lang-vertical {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: center;
            position: fixed;
            bottom: 0;
            gap: 1rem;
            text-align: center;
            z-index: 2;
            margin-bottom: 1rem;
            border-top: rgb(68, 84, 86) solid 1px;
            padding-top: 1rem;
        }
        .nav-items-vertical {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            position: fixed;
            top: 3.5rem;
            right: 0;
            gap: 1.75rem;
            height: 100%;
            background-color: rgba(88, 110, 114, 1);
            z-index: 1;

        }

        .nav-item {
            border-top: rgb(68, 84, 86) solid 1px;
            width: 100%;
            text-align: center;
            padding-top: 1rem;
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