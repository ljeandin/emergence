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
    <header>
        <nav class="header">
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
