<script setup>
    import { ref } from "vue";

    let is_more_infos_visible = ref(false);

    function toggleMoreInfosVisibility() {
        is_more_infos_visible.value =
            !is_more_infos_visible.value;
    }
</script>

<template>
    <section class="about-practice">
        <div class="about-practice__keywords">
            <span>harmonie</span>
            <span>équilibre</span>
            <span>habitat</span>
            <span>bonheur</span>
        </div>
        <h2 class="heading-1">
            Lorem ipsum dOlor sit amet, consectetur
            adipiscing elit, sed do eiusmod tempor
            incididunt ut labore et dolore magna aliqua. Ut
            enim ad minim veniam, quis nostrud exercitation
            ullamcO laboris nisi ut aliquip ex ea commodo
            consequat. Duis aute irure dolor in étOile
            VOlante reprehenderit in voluptate velit esse
            cillum dolore.
        </h2>
        <button
            class="button-discrete"
            @click="toggleMoreInfosVisibility()"
        >
            Lire plus
        </button>

        <div
            class="about-practice__infos"
            v-show="is_more_infos_visible"
        >
            <p>
                Lorem ipsum dOlor sit amet, consectetur
                adipiscing elit, sed do eiusmod tempor
                incididunt ut labore et dolore magna aliqua.
                Ut enim ad minim veniam, quis nostrud
                exercitation ullamcO laboris nisi ut aliquip
                ex ea commodo consequat. Duis aute irure
                dolor in étOile VOlante reprehenderit in
                voluptate velit esse cillum dolore.
            </p>
        </div>
    </section>
</template>
