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
                    <a class="nav-item">Tjenester</a>
                    <a class="nav-item">Om oss</a>
                    <a class="nav-item">Kontakt oss</a>
                    <a class="nav-item">Ledige stillinger</a>
                <div class="vertical-lang" :class="{'lang-vertical': isOpen}">
                    <a class="lang-option">EN</a>
                    <p class="lang-separator">|</p>
                    <a class="lang-option">NO</a>
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
        position: fixed;
        top: 0;
        width: 100%;
        z-index: 1;
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
        margin: 0;
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
        margin-bottom: 16px;
    }

    a {
        text-decoration: underline 1.5px rgba(196, 65, 17, 0);
        transition: 500ms;
        text-underline-offset: 4px;
    }
    .nav-item:hover, .lang-option:hover {
        cursor: pointer;
        text-decoration-color: rgba(196, 65, 17, 1);
    }

    .lang-option:hover {
        text-decoration: none;
        color: #c44111;
    }

    .lang-option {
        margin: 0;
        margin-top: 16px;
    }
    .lang-separator {
        cursor: default;
        margin: 0;
        margin-top: 16px;
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
            text-align: left;
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
            overflow: auto;
            top: 3.5rem;
            right: 0;
            gap: 0;
            height: 100%;
            width: 220px;
            background-color: rgba(88, 110, 114, 1);
            z-index: 1;
            animation-name: burger-slide;
            animation-duration: 0.5s;
        }

        @keyframes burger-slide {
            from { right: -240.18px;}
            to { right: 0;}
        }

        .nav-items-vertical a {
            padding: 10px 0 10px 0;
        }

        .nav-item {
            border-top: rgb(68, 84, 86) solid 1px;
            width: 100%;
            text-align: center;
            margin-top: 0;
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
    
    @media (max-height: 550px) and (max-width: 768px) {
            .nav-items-vertical {
                gap: 0.25rem;
            }

            .nav-item {
                margin-top: 0;
            }

            .lang-vertical {
                padding-top: 0;
                margin: 0;
                font-size: 12px;
            }
        }

        @media (max-height: 340px) and (max-width: 768px) {
            .nav-items-vertical {
                gap: 0;
            }

            .lang-vertical {
                display: none;
            }

            .lang {
                display: flex;
                position: fixed;
                top: -0;
                right: 2.5rem;
                font-size: 12px;
            }
        }
</style>