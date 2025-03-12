<script setup>
    const testimonials = [
        {
            picture: new URL(
                "@/assets/images/testimonials/marie.jpg",
                import.meta.url
            ).href,
            name: "Marie, 34 ans",
            review: "On the other hand, we denounce with righteous indignation and dislike men who are so beguiled and demoralized by the charms of pleasure of the moment, so blinded by desire, that they cannot foresee the pain and trouble that are bound to ensue; and equal blame belongs to those who fail in their duty through weakness of will, which is the same as saying through shrinking from toil and pain",
        },
        {
            picture: new URL(
                "@/assets/images/testimonials/josie.jpg",
                import.meta.url
            ).href,
            name: "Josie, 32 ans",
            review: "On the other hand, we denounce with righteous indignation and dislike men who are so beguiled and demoralized by the charms of pleasure of the moment, so blinded by desire, that they cannot foresee the pain and trouble that are bound to ensue; and equal blame belongs to those who fail in their duty through weakness of will, which is the same as saying through shrinking from toil and pain.",
        },
        {
            picture: new URL(
                "@/assets/images/testimonials/beatrice.jpg",
                import.meta.url
            ).href,
            name: "Béatrice, 43 ans",
            review: "On the other hand, we denounce with righteous indignation and dislike men who are so beguiled and demoralized by the charms of pleasure of the moment, so blinded by desire, that they cannot foresee the pain and trouble that are bound to ensue; and equal blame belongs to those who fail in their duty through weakness of will, which is the same as saying through shrinking from toil and pain",
        },
    ];
</script>

<template>
    <section class="testimonials">
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
                    {{ testimonial.name }}
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
