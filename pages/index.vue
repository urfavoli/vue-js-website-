<template>
  <main class="relative min-h-screen overflow-hidden bg-gray-900 text-white">
    <div
      class="background-animation absolute inset-0 -z-10"
      aria-hidden="true"
    />

    <section
      class="relative z-10 flex h-screen items-center justify-center p-6 text-center animate-fade-in-up"
    >
      <div class="space-y-6">
        <h1
          class="text-4xl font-extrabold sm:text-5xl lg:text-7xl"
        >
          <AnimatedText>Les Petits Pandas 🐼</AnimatedText>
        </h1>
        <p
          class="mx-auto max-w-2xl text-lg sm:text-xl lg:text-2xl opacity-0 animate-fade-in-up animation-delay-500"
        >
          Un monde de douceur et d'éveil pour vos enfants.
        </p>
        <nuxt-link
          to="/services"
          class="glow-on-hover-cta relative z-10 inline-flex justify-center items-center mt-8 rounded-full border border-green-400 px-6 py-3 text-base font-bold uppercase tracking-wide transition duration-300 ease-in-out sm:px-8 sm:py-4 sm:text-lg"
        >
          <span class="relative z-10 text-white">Découvrez nos services</span>
        </nuxt-link>
      </div>
      <img
        :src="getImageUrl('im1.jpeg')"
        alt="Enfants souriants jouant"
        class="absolute bottom-10 right-10 hidden h-48 w-48 rounded-full object-cover shadow-2xl lg:block animate-fade-in-up animation-delay-700"
      >
    </section>

    <section class="py-20 animate-fade-in-up animation-delay-1000">
      <div class="container mx-auto px-6 text-center">
        <h2 class="mb-12 text-4xl font-bold">
          <AnimatedText>Nos Services</AnimatedText>
        </h2>
        <div class="grid gap-8 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
          <div
            class="service-card group cursor-pointer rounded-xl bg-gray-800 p-8 shadow-lg transition duration-500 hover:scale-105 hover:bg-green-700 hover:shadow-2xl"
          >
            <h3
              class="mb-4 text-2xl font-semibold text-green-300 group-hover:text-white"
            >
              Activités d'éveil
            </h3>
            <p class="text-gray-300">
              Des jeux créatifs et éducatifs pour stimuler la curiosité de vos
              petits pandas.
            </p>
          </div>
          <div
            class="service-card group cursor-pointer rounded-xl bg-gray-800 p-8 shadow-lg transition duration-500 hover:scale-105 hover:bg-teal-700 hover:shadow-2xl"
          >
            <h3
              class="mb-4 text-2xl font-semibold text-teal-300 group-hover:text-white"
            >
              Repas Bio & Équilibrés
            </h3>
            <p class="text-gray-300">
              Des repas frais, locaux et adaptés à chaque régime alimentaire.
            </p>
          </div>
          <div
            class="service-card group cursor-pointer rounded-xl bg-gray-800 p-8 shadow-lg transition duration-500 hover:scale-105 hover:bg-blue-700 hover:shadow-2xl"
          >
            <h3
              class="mb-4 text-2xl font-semibold text-blue-300 group-hover:text-white"
            >
              Garderie Flexible
            </h3>
            <p class="text-gray-300">
              Des horaires adaptés à vos besoins et à ceux de vos enfants.
            </p>
          </div>
        </div>
        <img
          :src="getImageUrl('im2.jpeg')"
          alt="Enfants peignant et jouant"
          class="mx-auto mt-12 h-64 w-full max-w-lg rounded-xl object-cover shadow-xl animate-fade-in-up animation-delay-1200"
        >
      </div>
    </section>

    <section class="py-20 animate-fade-in-up animation-delay-1500">
      <div class="container mx-auto px-6 text-center">
        <h2 class="mb-12 text-4xl font-bold">
          <AnimatedText>Qui sommes-nous ?</AnimatedText>
        </h2>
        <div class="items-center md:flex md:space-x-8">
          <div class="mb-6 md:mb-0 md:w-1/2">
            <p class="text-lg leading-relaxed text-gray-300">
              "Les Petits Pandas" est un lieu chaleureux et sécurisé où chaque
              enfant peut s'épanouir à son rythme. Notre équipe de
              professionnels passionnés veille au bien-être, à l'éveil et à
              l'épanouissement de vos petits, dans un environnement stimulant
              et bienveillant.
            </p>
            <img
              :src="getImageUrl('im3.jpeg')"
              alt="Équipe pédagogique avec des enfants"
              class="mx-auto mt-8 h-56 w-full max-w-sm rounded-xl object-cover shadow-xl animate-fade-in-up animation-delay-1700 md:hidden"
            >
          </div>
          <div class="md:w-1/2">
            <img
              :src="getImageUrl('im3.jpeg')"
              alt="Aire de jeux intérieure colorée"
              class="h-64 w-full rounded-xl object-cover shadow-xl transition-transform duration-500 hover:scale-105 hover:rotate-3"
            >
          </div>
        </div>
      </div>
    </section>

    <section class="py-20 animate-fade-in-up animation-delay-2000">
      <div class="container mx-auto px-6 text-center">
        <h2 class="mb-12 text-4xl font-bold">
          <AnimatedText>Ce que disent nos parents</AnimatedText>
        </h2>
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div class="bg-gray-800 p-8 rounded-xl shadow-xl border border-gray-700">
            <p class="italic text-gray-300 mb-4">
              "Une équipe formidable et un environnement très sûr. Mon enfant est
              toujours impatient de venir à la garderie!"
            </p>
            <p class="font-semibold text-white">
              - Marie S.
            </p>
          </div>
          <div class="bg-gray-800 p-8 rounded-xl shadow-xl border border-gray-700">
            <p class="italic text-gray-300 mb-4">
              "Les activités sont créatives et variées. Je suis impressionné par
              l'apprentissage de mon enfant."
            </p>
            <p class="font-semibold text-white">
              - John D.
            </p>
          </div>
          <div class="bg-gray-800 p-8 rounded-xl shadow-xl border border-gray-700">
            <p class="italic text-gray-300 mb-4">
              "Les Petits Pandas, c'est comme une seconde famille. On se sent vraiment
              écoutés et soutenus."
            </p>
            <p class="font-semibold text-white">
              - Sophie B.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section class="py-20 animate-fade-in-up animation-delay-2500">
      <div class="container mx-auto px-6 text-center">
        <h2 class="mb-8 text-4xl font-bold">
          <AnimatedText>Inscrivez votre enfant dès aujourd'hui !</AnimatedText>
        </h2>
        <p class="mb-8 text-lg text-gray-300">
          Les places sont limitées pour assurer un suivi personnalisé et de
          qualité. Réservez la place de votre enfant dans notre famille "Les
          Petits Pandas".
        </p>
        <button
          class="glow-on-hover mt-4 rounded-full border border-green-400 px-8 py-4 text-lg font-bold uppercase tracking-wide transition duration-300 ease-in-out"
        >
          Contactez-nous pour une visite
        </button>
        <div
          class="mt-12 grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-2"
        >
          <img
            :src="getImageUrl('im4.jpeg')"
            alt="Activités extérieures pour enfants"
            class="h-64 w-full rounded-xl object-cover shadow-lg animate-fade-in-up animation-delay-2700"
          >
          <img
            :src="getImageUrl('im5.jpeg')"
            alt="Moment de lecture avec les enfants"
            class="h-64 w-full rounded-xl object-cover shadow-lg animate-fade-in-up animation-delay-2900"
          >
        </div>
      </div>
    </section>
  </main>
</template>

<script lang="ts" setup>
// Métadonnées de la page et fonctions utilitaires
useHead({
  title: "Les Petits Pandas - Garderie d'enfants",
  meta: [
    {
      name: 'description',
      content:
        "Découvrez 'Les Petits Pandas', une garderie chaleureuse et stimulante..."
    },
    {
      name: 'keywords',
      content:
        'garderie, crèche, enfants, éveil, activités enfants, Les Petits Pandas'
    },
    {
      property: 'og:title',
      content: 'Les Petits Pandas - Garderie'
    }
  ]
})

function getImageUrl (name: string) {
  return `/images/${name}`
}
</script>

<style scoped>
/* Nouveaux délais pour la nouvelle section et le CTA */
.animation-delay-2000 { animation-delay: 2s; }
.animation-delay-2500 { animation-delay: 2.5s; }
.animation-delay-2700 { animation-delay: 2.7s; }
.animation-delay-2900 { animation-delay: 2.9s; }



.service-card:hover {
  box-shadow: 0 0 15px rgba(0, 255, 200, 0.7);
}
</style>
