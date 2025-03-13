<script setup>
    import { ref, watch } from "vue";

    const isMenuOpen = ref(false);
    const isFullyHidden = ref(true);

    const toggleMenu = () => {
        isMenuOpen.value === true
            ? ((isMenuOpen.value = false),
              setTimeout(
                  () => (isFullyHidden.value = true),
                  300
              ))
            : ((isFullyHidden.value = false),
              setTimeout(
                  () => (isMenuOpen.value = true),
                  300
              ));
    };

    const navLinks = [
        { name: "Accueil", link: "#" },
        { name: "Le feng-shui", link: "#" },
        { name: "Témoignages", link: "#" },
        { name: "Services", link: "#" },
        { name: "À propos", link: "#" },
        { name: "Réservation", link: "#" },
    ];
</script>

<template>
    <header class="header">
        <h1 class="header__title heading-4">
            Émergence feng-shui
        </h1>
        <button
            class="header__burger-menu button-icon"
            :class="{
                'header__burger-menu--open': isMenuOpen,
            }"
            @click="toggleMenu"
        >
            <img
                src="@/assets/images/header/menu_icon.svg"
                alt=""
            />
        </button>

        <nav
            class="header__links-wrapper"
            :class="{
                'header__links-wrapper--visible':
                    isMenuOpen,
                'header__links-wrapper--hidden':
                    isFullyHidden,
            }"
        >
            <span v-for="link in navLinks">
                <a
                    class="header__link"
                    :key="link.name"
                    :href="link.link"
                    @click="isMenuOpen = false"
                >
                    {{ link.name }}
                </a>
            </span>
        </nav>
    </header>
</template>
