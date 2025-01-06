<template>
  <NuxtLayout>
    <NuxtLoadingIndicator />

    <header class="hero is-primary is-bold">
      <div class="hero-body">
        <div class="container">
          <div class="level is-flex is-justify-content-center is-align-content-center">
            <h1 class="title">
              <NuxtLink to="/">
                <img alt="le Blog de Jean Luc Houédanou" src="/images/articles/logo-mini.svg" height="320">
              </NuxtLink>
            </h1>
          </div>
        </div>
      </div>
    </header>
    <main class="section">
      <NuxtPage />
    </main>
  </NuxtLayout>
</template>

<script setup>
import LanguageSwitcher from '~/components/LanguageSwitcher.vue'

useHead({
  title: 'Le blog de Big Five '
});
</script>

<style lang="scss">
html {
  background: #EEE;
}

main {
  background: #EEE;
}
</style>