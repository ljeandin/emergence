<script setup>
    const offers = [
        {
            title: "1er pilier",
            subtitle: "Le rapport d’expertise",
            type: "paragraph",
            content: `Une analyse complète de ton habitat selon les principes du Feng Shui traditionnel (l'école de la forme,
              sectorisation Bagua et carré LoShu, manques/extensions, les 8 palais des habitants, leurs orientations favorables,
              les remèdes et activateurs liés aux étoiles volantes), <b>guidée par des vidéos explicatives</b> et un
              <b>calendrier “plan d’action”</b>.`,
        },
        {
            title: "2ème pilier",
            subtitle: "L’accompagnement",
            type: "list",
            content: [
                `<b>1 Atelier d’intention Feng Shui par mois</b> posez vos intentions, partagez vos expériences et renforcez votre connexion à votre environnement.`,
                `<b>1 Séance de questions/réponses par semaine :</b> affine ta compréhension et co-construire des solutions décoratives adaptées à ton espace.`,
                `<b>1 Communauté bienveillante et inspirante</b> où tu pourras partager ton parcours, poser tes questions et célébrer tes avancées.`,
            ],
        },
        {
            title: "3ème pilier",
            subtitle: "L’ancrage",
            type: "list",
            content: [
                `<b>3 Méditations guidées :</b> elles te guideront au fur et à mesure de l’accompagnement pour manifester la transformation que tu mérites.`,
                `<b>Découvertes symboliques, purification et lithothérapie:</b> utilise des objets porteurs de sens et intègre la lithothérapie dans les pièces principales. Il est essentiel de rafraichir l’énergie qui a stagné et de se débarrasser des énergies négatives.`,
            ],
        },
    ];

    const part_image_URL_maker = function (imageNumber) {
        return new URL(
            `../../../assets/images/offer/offer_part_${imageNumber}.jpg`,
            import.meta.url
        ).href;
    };
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
            >
                Découvre les 3 piliers essentiels à ton
                épanouissement
            </a>
        </div>

        <div
            v-for="(offer, index) in offers"
            :key="index"
            class="offer-part"
        >
            <img
                class="offer-part__image"
                :src="part_image_URL_maker(index + 1)"
                alt=""
            />
            <div class="offer-part__text">
                <h2 class="offer-part__title heading-2">
                    {{ offer.title }} :
                    <em>{{ offer.subtitle }}</em>
                </h2>
                <div v-if="offer.type === 'paragraph'">
                    <p v-html="offer.content"></p>
                </div>
                <ul v-else>
                    <li
                        v-for="(item, idx) in offer.content"
                        :key="idx"
                        v-html="item"
                    ></li>
                </ul>
            </div>
        </div>
    </section>
</template>
