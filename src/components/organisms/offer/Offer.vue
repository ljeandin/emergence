<script setup>
    import { ref } from "vue";

    const offers = [
        {
            title: "1er pilier",
            subtitle: "Le rapport d’expertise",
            type: "paragraph",
            content: `Grâce à une <b>analyse détaillée</b>, vous comprenez comment votre environnement influence votre énergie et votre bien-être.<br />
En s’appuyant sur la sectorisation Bagua, le carré LoShu et les 8 palais, l’analyse révèle comment optimiser chaque espace selon les besoins spécifiques de chaque habitant.<br />
Les étoiles volantes aident à corriger les déséquilibres énergétiques et à stimuler la chance, la santé et la prospérité. <br />
Le <b>calendrier “plan d’action”</b> offre une feuille de route claire pour mettre en place les ajustements au bon moment, maximisant les résultats sur le long terme. Il vous aidera à prioriser selon les recommandations.<br />
Vous obtiendrez une <b>méthode complète et guidée</b> pour transformer votre espace de vie en un véritable allié énergétique, aligné avec vos objectifs et votre bien-être.`,
        },
        {
            title: "2ème pilier",
            subtitle: "L’accompagnement",
            type: "list",
            content: [
                `<b>1 Atelier d’intention Feng Shui collectif d'une heure par mois</b> posez vos intentions, partagez vos expériences et renforcez votre connexion à votre environnement.`,
                `<b>1 Séance de questions/réponses d'une heure par semaine :</b> affinez votre compréhension et co-construisons des solutions décoratives adaptées à votre espace.`,
                `<b>1 Communauté privée bienveillante et inspirante</b> où vous pourrez partager votre parcours, poser vos questions et célébrer vos avancées.`,
            ],
        },
        {
            title: "3ème pilier",
            subtitle: "L’ancrage",
            type: "list",
            content: [
                `<b>Accès à 1 audio par mois :</b> il vous guidera au fur et à mesure de l’accompagnement pour manifester la transformation que vous méritez.`,
                `<b>Découvertes symboliques, purification et lithothérapie:</b> utilisez des objets porteurs de sens et intègrez la lithothérapie dans les pièces principales. Il est essentiel de rafraichir l’énergie qui a stagné et de se débarrasser des énergies négatives.`,
            ],
        },
    ];

    const part_image_URL_maker = function (imageNumber) {
        return new URL(
            `../../../assets/images/offer/offer_part_${imageNumber}.webp`,
            import.meta.url
        ).href;
    };

    let is_more_infos_visible = ref(false);

    function toggleMoreInfosVisibility() {
        is_more_infos_visible.value =
            !is_more_infos_visible.value;
    }
</script>

<template>
    <section
        class="offer"
        id="services"
    >
        <div class="offer__header">
            <p class="heading-1">
                Transforme ton espace, libère ton énergie :
                je t’accompagne durant 3 mois en ligne pour
                réveiller ta vitalité et booster ta réussite
                grâce au Feng Shui traditionnel.
            </p>
            <button
                class="button-discrete"
                @click="toggleMoreInfosVisibility()"
            >
                Plongez au cœur de mon accompagnement
                sur-mesure.
            </button>

            <div v-show="is_more_infos_visible">
                <h3 class="heading-2">
                    Votre espace, votre énergie : un
                    accompagnement Feng Shui personnalisé
                </h3>

                <br />

                <p class="offer__details">
                    Au-delà des principes décoratifs souvent
                    associés au Feng Shui, j’utilise une
                    méthode d’analyse avancée appelée "les
                    étoiles volantes". Il s’agit d’une
                    cartographie énergétique qui croise
                    trois dimensions essentielles :<br /><br />
                    <b>Le temps :</b> chaque période
                    influence la qualité et la nature des
                    énergies présentes.<br />
                    <b>L’espace :</b> l’agencement du lieu
                    et son orientation jouent un rôle clé
                    dans la répartition des flux
                    énergétiques.<br />
                    <b>Les personnes :</b> chaque individu
                    possède un chiffre kua ou ming gua
                    déterminant des directions personnelles
                    favorables, influençant son sommeil, sa
                    concentration ou sa vitalité.<br /><br />
                    En croisant ces données, on obtient une
                    lecture précise du potentiel énergétique
                    de votre maison. L’objectif est de
                    capter et de diriger le Chi de manière
                    optimale pour qu’il devienne votre allié
                    au quotidien plutôt qu’une source
                    invisible de blocages, de fatigue ou de
                    tensions.<br />
                </p>

                <br />

                <h4 class="heading-3">
                    À qui s’adresse cette offre ?
                </h4>
                <br />
                <p class="offer__details">
                    <b
                        >Les particuliers et les
                        professionnels :</b
                    >
                    <br /><br />
                    Qui sont en création des plans de leur
                    futur maison et qui souhaitent
                    déterminer le placement des pièces.<br />
                    <br />
                    Qui emménagent et qui ont des projets
                    décoratifs et souhaitant bénéficier des
                    meilleures énergies.<br />
                    <br />
                    Qui ont envie de renouveau et d’avancer
                    dans leur vie.<br />
                    <br />
                    Qui travaillent de chez eux, pour créer
                    un cadre propice à la réussite et à
                    l’abondance.<br />
                </p>

                <br />

                <h4 class="heading-3">
                    Déroulement de l’offre :
                </h4>
                <br />
                <p class="offer__details">
                    <b>Entretien initial</b> en visio pour
                    échanger sur votre situation et définir
                    vos objectifs.<br />
                    <b>Analyse</b> de votre plan et
                    cartographie énergétique de votre espace
                    de vie.<br />
                    <b>Rapport détaillé</b> incluant des
                    recommandations pratiques pour
                    harmoniser les énergies et corriger les
                    déséquilibres.<br />
                    <b>Suivi</b> de 3 mois en collectif.<br />
                    <br />
                </p>

                <h4 class="heading-3">
                    Documents à fournir :
                </h4>

                <br />

                <ul class="offer__details">
                    <br />
                    <li>Photos</li>
                    <li>Plan à l’échelle</li>
                    <li>
                        Orientation de la porte d’entrée
                        selon mes instructions
                    </li>
                    <li>Questionnaires habitant/habitat</li>
                </ul>

                <br />

                <h4 class="heading-3">Tarif :</h4>
                <br />
                <p class="offer__details">
                    1750€ ou trois mensualités de 620€
                </p>
            </div>
        </div>

        <div
            v-for="(offer, index) in offers"
            :key="index"
            class="offer-part"
            id="les-piliers"
        >
            <img
                class="offer-part__image"
                :src="part_image_URL_maker(index + 1)"
                alt=""
            />
            <div class="offer-part__text">
                <h2 class="offer-part__title heading-2">
                    {{ offer.title }}&nbsp:
                    <em>{{ offer.subtitle }}</em>
                </h2>
                <div v-if="offer.type === 'paragraph'">
                    <p v-html="offer.content"></p>
                </div>
                <ul v-else>
                    <li
                        v-for="(
                            item, index
                        ) in offer.content"
                        :key="index"
                        v-html="item"
                    ></li>
                </ul>
            </div>
        </div>
    </section>
</template>
