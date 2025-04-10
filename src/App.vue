<script setup>
    import Header from "./components/organisms/header/Header.vue";
    import Hero from "./components/organisms/hero/Hero.vue";
    import AboutPractice from "./components/organisms/about-practice/AboutPractice.vue";
    import Testimonials from "./components/organisms/testimonials/Testimonials.vue";
    import Offer from "./components/organisms/offer/Offer.vue";
    import About from "./components/organisms/about/About.vue";
    import Footer from "./components/organisms/footer/Footer.vue";
</script>

<template>
    <Header />
    <main>
        <Hero />
        <AboutPractice />
        <Testimonials />
        <img
            class="decorative-banner"
            src="/src/assets/images/banners/banner_decorative_1.webp"
            alt=""
            style="object-position: 56%"
        />
        <Offer />
        <img
            class="decorative-banner"
            src="/src/assets/images/banners/banner_decorative_2.webp"
            alt=""
            style="object-position: 7%"
        />
        <About />
        <Footer />
    </main>
</template>
