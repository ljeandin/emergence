<script setup>
    import Header from "./components/organisms/header/Header.vue";
    import Hero from "./components/organisms/hero/Hero.vue";
    import AboutPractice from "./components/organisms/about-practice/AboutPractice.vue";
    import Testimonials from "./components/organisms/testimonials/Testimonials.vue";
</script>

<template>
    <Header />
    <Hero />
    <AboutPractice />
    <Testimonials />
    <img
        class="decorative-banner"
        src="/src/assets/images/banners/banner_grass.jpg"
        alt=""
    />
</template>
