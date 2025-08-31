<template>
  <div class="relative min-h-screen overflow-hidden bg-gray-900 text-white">
    <div
      class="background-animation absolute inset-0 -z-10"
      aria-hidden="true"
    />

    <main class="py-20 lg:py-32">
      <section class="container mx-auto px-6 text-center animate-fade-in-up">
        <h1 class="text-5xl font-extrabold text-shadow-glow mb-4">
          Nos Services Uniques
        </h1>
        <p class="text-xl max-w-2xl mx-auto text-gray-400">
          Découvrez les différentes activités et prestations que nous offrons
          pour l'épanouissement de vos enfants.
        </p>
      </section>

      <section class="py-20 animate-fade-in-up animation-delay-500">
        <div class="container mx-auto px-6">
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-12">
            <div class="service-card group cursor-pointer rounded-xl bg-gray-800 p-8 shadow-lg transition-transform duration-500 hover:scale-105 hover:bg-green-700 hover:shadow-2xl">
              <span class="i-carbon-pedestrian-kid text-4xl text-green-300 group-hover:text-white mb-4" />
              <h3 class="mb-2 text-2xl font-semibold text-green-300 group-hover:text-white">
                Activités d'Éveil
              </h3>
              <p class="text-gray-300">
                Nous proposons un programme riche en ateliers créatifs et éducatifs,
                incluant la peinture, la musique, et la lecture pour stimuler
                leur curiosité et leur imagination.
              </p>
            </div>

            <div class="service-card group cursor-pointer rounded-xl bg-gray-800 p-8 shadow-lg transition-transform duration-500 hover:scale-105 hover:bg-teal-700 hover:shadow-2xl">
              <span class="i-carbon-food-grain text-4xl text-teal-300 group-hover:text-white mb-4" />
              <h3 class="mb-2 text-2xl font-semibold text-teal-300 group-hover:text-white">
                Repas Bio & Équilibrés
              </h3>
              <p class="text-gray-300">
                Des repas frais, locaux et biologiques sont préparés quotidiennement
                pour assurer la meilleure nutrition à vos enfants, en respectant
                toutes les allergies.
              </p>
            </div>

            <div class="service-card group cursor-pointer rounded-xl bg-gray-800 p-8 shadow-lg transition-transform duration-500 hover:scale-105 hover:bg-blue-700 hover:shadow-2xl">
              <span class="i-carbon-time text-4xl text-blue-300 group-hover:text-white mb-4" />
              <h3 class="mb-2 text-2xl font-semibold text-blue-300 group-hover:text-white">
                Horaires Flexibles
              </h3>
              <p class="text-gray-300">
                Nous comprenons les défis des parents. C'est pourquoi nous
                offrons des options d'horaires flexibles, adaptées à vos besoins
                quotidiens.
              </p>
            </div>
          </div>
        </div>
      </section>

      <section class="py-20 animate-fade-in-up animation-delay-1000">
        <div class="container mx-auto px-6 text-center">
          <h2 class="text-4xl font-bold text-shadow-glow mb-8">
            Ce que disent les parents
          </h2>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div class="bg-gray-800 p-6 rounded-lg shadow-xl">
              <p class="italic text-gray-300 mb-4">
                "Une équipe formidable et un environnement sûr. Mon enfant est toujours
                heureux de venir ici."
              </p>
              <p class="font-semibold text-white">
                - Sophie D.
              </p>
            </div>
            <div class="bg-gray-800 p-6 rounded-lg shadow-xl">
              <p class="italic text-gray-300 mb-4">
                "Les activités d'éveil sont incroyables. J'ai vu mon enfant progresser
                énormément en un an."
              </p>
              <p class="font-semibold text-white">
                - Marc L.
              </p>
            </div>
            <div class="bg-gray-800 p-6 rounded-lg shadow-xl">
              <p class="italic text-gray-300 mb-4">
                "Les repas sont de haute qualité, ce qui est très important pour nous.
                Je recommande vivement Les Petits Pandas."
              </p>
              <p class="font-semibold text-white">
                - Isabelle R.
              </p>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup>
// Métadonnées de la page pour le SEO
useHead({
  title: 'Nos Services - Les Petits Pandas',
  meta: [
    { name: 'description', content: 'Découvrez tous les services et activités proposés par Les Petits Pandas : repas bio, activités d\'éveil, horaires flexibles et plus encore.' }
  ]
})
</script>

<style scoped>
.animation-delay-500 { animation-delay: 0.5s; }
.animation-delay-1000 { animation-delay: 1s; }

.service-card:hover {
  box-shadow: 0 0 15px rgba(0, 255, 200, 0.7);
}
</style>
