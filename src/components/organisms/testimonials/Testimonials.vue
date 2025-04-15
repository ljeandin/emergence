<script setup>
    const testimonials = [
        {
            name: " Hilda",
            review: "Charlotte est une personne douce et humble, avec une réelle expertise. J’ai toujours apprécié son professionnalisme, sa patience et son sens du détail. Elle sait créer un climat de confiance et apporter des solutions adaptées, ce qui fait toute la différence.",
        },
        {
            name: "Maëlle",
            review: "Te côtoyer et travailler avec toi a été un vrai bonheur. Ta serviabilité, ton professionnalisme et ton envie d’apprendre font de toi une personne inspirante. Ton énergie positive et ta bonne humeur constante sont des atouts précieux.",
        },
        {
            name: "Patricia",
            review: "J’ai eu la chance de travailler avec Charlotte et j’ai toujours admiré sa motivation, son écoute et sa bienveillance. C’est une personne de confiance, avec de belles valeurs humaines.",
        },
    ];
</script>

<template>
    <section
        class="testimonials"
        id="temoignages"
    >
        <div class="testimonials__content-wrapper">
            <h2 class="testimonials__title heading-3">
                <i>Elles parlent de moi :</i>
            </h2>
            <div
                v-for="(testimonial, index) in testimonials"
                :key="index"
                class="testimonial"
            >
                <div class="testimonial__text">
                    <h2
                        class="testimonial__title heading-4"
                    >
                        {{ testimonial.name }},
                        <i class="heading-4">
                            ancienne collègue
                        </i>
                    </h2>
                    <img
                        class="testimonial__quote-icon"
                        src="/src/assets/images/testimonials/quote-icon.svg"
                        alt=""
                    />
                    <p>{{ testimonial.review }}</p>
                </div>
            </div>
        </div>
    </section>
</template>
