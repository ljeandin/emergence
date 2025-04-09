<script setup>
    const testimonials = [
        {
            picture: new URL(
                "@/assets/images/testimonials/marie.jpg",
                import.meta.url
            ).href,
            name: " Hilda",
            review: "Charlotte est une personne douce et humble, avec une réelle expertise. J’ai toujours apprécié son professionnalisme, sa patience et son sens du détail. Elle sait créer un climat de confiance et apporter des solutions adaptées, ce qui fait toute la différence.",
        },
        {
            picture: new URL(
                "@/assets/images/testimonials/josie.jpg",
                import.meta.url
            ).href,
            name: "Maëlle",
            review: "Te côtoyer et travailler avec toi a été un vrai bonheur. Ta serviabilité, ton professionnalisme et ton envie d’apprendre font de toi une personne inspirante. Ton énergie positive et ta bonne humeur constante sont des atouts précieux.",
        },
        {
            picture: new URL(
                "@/assets/images/testimonials/beatrice.jpg",
                import.meta.url
            ).href,
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
        <div
            v-for="(testimonial, index) in testimonials"
            :key="index"
            class="testimonial"
        >
            <img
                class="testimonial__image"
                :src="testimonial.picture"
                alt=""
            />
            <div class="testimonial__text">
                <h2 class="testimonial__title heading-2">
                    {{ testimonial.name }},
                    <i class="heading-3"
                        >ancienne collègue</i
                    >
                </h2>
                <img
                    class="testimonial__quote-icon"
                    src="/src/assets/images/testimonials/quote-icon.svg"
                    alt=""
                />
                <p>{{ testimonial.review }}</p>
            </div>
        </div>
    </section>
</template>
