<template>
    <div class="layout">

        <main class="main">
            <slot />
        </main>

        <footer class="footer">
            <div class="footer-content">
                <p>&copy; {{ new Date().getFullYear() }} Big Five. Tous droits réservés.</p>
                <!-- <div class="social-icons">
                    <a href="https://linkedin.com/in/votre-profil" target="_blank" rel="noopener noreferrer"><i
                            class="fab fa-linkedin"></i></a>
                    <a href="https://facebook.com/votre-page" target="_blank" rel="noopener noreferrer"><i
                            class="fab fa-facebook"></i></a>
                    <a href="https://github.com/votre-profil" target="_blank" rel="noopener noreferrer"><i
                            class="fab fa-github"></i></a>
                    <a href="https://instagram.com/votre-profil" target="_blank" rel="noopener noreferrer"><i
                            class="fab fa-instagram"></i></a>
                    <a href="https://twitter.com/votre-profil" target="_blank" rel="noopener noreferrer"><i
                            class="fab fa-twitter"></i></a>
                </div> -->
            </div>
        </footer>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

// const isDarkMode = ref(false)

// const toggleDarkMode = () => {
//     isDarkMode.value = !isDarkMode.value
//     document.body.classList.toggle('dark-mode', isDarkMode.value)
//     localStorage.setItem('darkMode', isDarkMode.value)
// }

// onMounted(() => {
//     const savedDarkMode = localStorage.getItem('darkMode')
//     if (savedDarkMode !== null) {
//         isDarkMode.value = JSON.parse(savedDarkMode)
//         document.body.classList.toggle('dark-mode', isDarkMode.value)
//     }
// })
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Source+Sans+Pro:wght@400;600&display=swap');

.layout {
    font-family: 'Source Sans Pro', sans-serif;
    color: var(--text-color);
    background-color: var(--bg-color);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

.header {
    border-bottom: 1px solid var(--border-color);
    padding: 1rem 0;
    position: sticky;
    top: 0;
    background-color: var(--bg-color);
    z-index: 1000;
}

.header-content,
.footer-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-family: 'Merriweather', serif;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--text-color);
    text-decoration: none;
}

.nav {
    display: flex;
    gap: 1rem;
}

.nav-link {
    color: var(--text-color);
    text-decoration: none;
    font-weight: 600;
    transition: color 0.3s ease;
}

.nav-link:hover {
    color: var(--accent-color);
}

.main {
    flex-grow: 1;
    padding: 2rem 1rem;
}

.footer {
    border-top: 1px solid var(--border-color);
    padding: 1rem 0;
    margin-top: 2rem;
}

.social-links {
    display: flex;
    gap: 1rem;
}

.social-link {
    color: var(--text-color);
    text-decoration: none;
    font-size: 0.9rem;
    transition: color 0.3s ease;
}

.social-link:hover {
    color: var(--accent-color);
}

:root {
    --text-color: #292929;
    --bg-color: #ffffff;
    --border-color: #e6e6e6;
    --accent-color:#71368b;
}

body.dark-mode {
    --text-color: #e6e6e6;
    --bg-color: #1a1a1a;
    --border-color: #4a4a4a;
    --accent-color:#71368b;
}

.social-icons {
    margin-top: 2rem;
}

.social-icons a {
    color: #333;
    font-size: 1.5rem;
    margin-right: 1rem;
    transition: color 0.3s ease;
}

.social-icons a:hover {
    color: #0077b5;
    /* Couleur LinkedIn comme exemple */
}
</style>