<script setup>
    import { ref } from "vue";

    let is_more_infos_visible = ref(false);

    function toggleMoreInfosVisibility() {
        is_more_infos_visible.value =
            !is_more_infos_visible.value;
    }
</script>

<template>
    <section
        class="about-practice"
        id="le-feng-shui"
    >
        <div class="about-practice__keywords">
            <span>harmonie</span>
            <span>équilibre</span>
            <span>habitat</span>
            <span>bonheur</span>
        </div>
        <h2 class="heading-1">
            “Le Feng Shui est à l'environnement ce que
            l'acupuncture est au corps" <br />
            Van Minh
        </h2>
        <button
            class="button-discrete"
            @click="toggleMoreInfosVisibility()"
        >
            Découvre le Feng Shui
        </button>

        <div
            class="about-practice__infos"
            v-show="is_more_infos_visible"
        >
            <img
                class="about-practice__image"
                src="@/assets/images/about_feng_shui/about_feng_shui.jpg"
                alt=""
                width="300"
                height="300"
            />

            <h2
                class="about-practice__infos-title heading-2"
            >
                Qu’est-ce que le Feng Shui traditionnel et
                comment il vous transforme ?
            </h2>

            <p>
                Le Feng Shui révèle comment l’énergie qui
                circule autour de nous, influence notre état
                d’esprit, nos émotions, et même nos
                opportunités. <br />
                <br />
                Le Feng Shui, c’est avant tout l’art de
                rééquilibrer et d’optimiser la circulation
                de l’énergie vitale qui est le Chi ou QI,
                dans votre espace de vie. On pourrait le
                comparer à une forme d’acupuncture de
                l’habitat : au lieu d’aiguilles, nous
                utilisons des outils spécifiques et des
                ajustements stratégiques comme les couleurs
                et les matières, pour lever les blocages
                énergétiques, rétablir l’harmonie et aligner
                les énergies afin de soutenir vos objectifs
                de vie. <br />
                <br />
                Chaque recommandation repose sur le principe
                des cinq éléments (Bois, Feu, Terre, Métal,
                Eau) et le Yin et Yang, qui interagissent
                entre eux pour créer un équilibre. C’est
                grâce au Feng Shui traditionnel, notamment
                la méthode des étoiles volantes et nos
                directions favorables que la vraie
                transformation peut s’opérer.
            </p>

            <h3
                class="about-practice__infos-title heading-3"
            >
                Quels en sont les bénéfices ?
            </h3>
            <ul>
                <li>
                    Renforcement des liens affectifs
                    (partenaire, enfants, entourage proche)
                </li>

                <li>
                    Déploiement de vos talents et de votre
                    mission de vie
                </li>

                <li>
                    Fluidification des projets concrets et
                    des flux financiers
                </li>

                <li>
                    Retrouver vitalité, équilibre et
                    légèreté au quotidien
                </li>
                <li>
                    Améliorer la qualité et la profondeur du
                    sommeil
                </li>

                <li>
                    Stimuler l’attention, la clarté d’esprit
                    et la motivation
                </li>

                <li>
                    Booster la croissance de votre
                    entreprise ou activité indépendante
                </li>
                <li>
                    Élever la vibration énergétique de vos
                    lieux
                </li>
            </ul>
        </div>
    </section>
</template>
