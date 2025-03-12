<script setup>
    const offer_part = [
        {
            picture: new URL(
                "@/assets/images/offer/offer_part_1.jpg",
                import.meta.url
            ).href,
            title: "1er pilier : Le rapport d’expertise",
            content:
                "Une analyse complète de ton habitat selon les principes du Feng Shui traditionnel (l'école de la forme, sectorisation Bagua et carré LoShu, manques/extensions, les 8 palais des habitants, leurs orientations favorables, les remèdes et activateurs liés aux étoiles volantes), guidée par des vidéos explicatives et un calendrier “plan d’action”.",
        },
        {
            picture: new URL(
                "@/assets/images/offer/offer_part_2.jpg",
                import.meta.url
            ).href,
            title: "2 ème pilier : L’accompagnement",
            content:
                "- 1 Atelier d’intention Feng Shui par mois posez vos intentions, partagez vos expériences et renforcez votre connexion à votre environnement. - 1 Séance de questions/réponses par semaine :  affine ta compréhension et co-construire des solutions décoratives adaptées à ton espace. - 1 Communauté bienveillante et inspirante où tu pourras partager ton parcours, poser tes questions et célébrer tes avancées.",
        },
        {
            picture: new URL(
                "@/assets/images/offer/offer_part_3.jpg",
                import.meta.url
            ).href,
            title: "3 ème pilier : L’ancrage",
            content:
                "3 Méditations guidées : elles te guideront au fur et à mesure de l’accompagnement pour manifester la transformation que tu mérites. Découvertes symboliques, purification et lithothérapie : utilise des objets porteurs de sens et intègre la lithothérapie dans les pièces principales. Il est essentiel de rafraichir l’énergie qui a stagné et de se débarrasser des énergies négatives.",
        },
    ];
</script>

<template>
    <section class="offer">
        <div class="offer__header">
            <h2 class="heading-3">
                L'accompagnement "Profondeur Énergétique"
            </h2>
            <p class="heading-1">
                Un accompagnement à distance de 3 mois pour
                transformer ton habitat en une source
                d’énergie pOsitive et retrouver ton
                équilibre, ta vitalité et ton bien-être,
                tant personnel que professionnel, grâce au
                Feng Shui traditionnel.
            </p>
            <a
                class="button-discrete"
                href=""
                >Découvre les 3 piliers essentiels à ton
                épanouissement</a
            >
        </div>
        <div
            v-for="(part, index) in offer_part"
            :key="index"
            class="offer-part"
        >
            <img
                class="offer-part__image"
                :src="part.picture"
                alt=""
            />
            <div class="offer-part__text">
                <h2 class="offer-part__title heading-2">
                    {{ part.title }}
                </h2>
                <p>{{ part.content }}</p>
            </div>
        </div>
    </section>
</template>
