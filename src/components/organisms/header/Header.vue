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
        { name: "Accueil", link: "#accueil" },
        { name: "Le feng shui", link: "#le-feng-shui" },
        { name: "Témoignages", link: "#temoignages" },
        { name: "Services", link: "#services" },
        { name: "À propos", link: "#a-propos" },
        {
            name: "Réservation",
            link: "https://calendar.app.google/pPjXiihbKo3CW7Xs6",
        },
    ];
</script>

<template>
    <header class="header">
        <a
            href="#accueil"
            class="heading-4 header__logo--mobile"
        >
            <img
                src="@/assets/images/header/logo.webp"
                class="header__logo"
                alt="Émergence Feng Shui"
            />
        </a>

        <button
            class="header__burger-menu button-icon"
            :class="{
                'header__burger-menu--open': isMenuOpen,
            }"
            @click="toggleMenu"
            aria-labelledby="button-label-menu"
        >
            <span
                id="button-label-menu"
                hidden
                >Menu</span
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
            <span v-for="link in navLinks.slice(0, 3)">
                <a
                    class="header__link"
                    :key="link.name"
                    :href="link.link"
                    @click="isMenuOpen = false"
                >
                    {{ link.name }}
                </a>
            </span>
            <a
                href="#accueil"
                class="heading-4 header__logo--desktop"
            >
                <img
                    src="@/assets/images/header/logo.webp"
                    class="header__logo"
                    alt="Émergence Feng Shui"
                />
            </a>
            <span v-for="link in navLinks.slice(3)">
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
