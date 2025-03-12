<script setup>
    const navLinks = [
        {
            name: "Accueil",
            link: "#",
        },
        {
            name: "Le feng-shui",
            link: "#",
        },
        {
            name: "Témoignages",
            link: "#",
        },
        {
            name: "Services",
            link: "#",
        },
        {
            name: "À propos",
            link: "#",
        },
        {
            name: "Réservation",
            link: "#",
        },
    ];
</script>

<template>
    <header class="header">
        <nav class="header__links-wrapper">
            <a
                class="header__link"
                v-for="link in navLinks"
                :href="link.link"
            >
                {{ link.name }}
            </a>
        </nav>
    </header>
</template>
