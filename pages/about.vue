<template>
  <div class="relative min-h-screen overflow-hidden bg-gray-900 text-white">
    <div
      class="background-animation absolute inset-0 -z-10"
      aria-hidden="true"
    />

    <main class="py-20 lg:py-32">
      <section class="container mx-auto px-6 text-center animate-fade-in-up">
        <h1 class="text-5xl font-extrabold text-shadow-glow mb-4">
          Qui sommes-nous ?
        </h1>
        <p class="text-xl max-w-2xl mx-auto text-gray-400">
          Découvrez l'équipe passionnée et les valeurs qui animent "Les Petits Pandas".
        </p>
      </section>

      <section class="py-20 animate-fade-in-up animation-delay-500">
        <div class="container mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
          <div class="md:order-1">
            <h2 class="text-4xl font-bold text-shadow-glow mb-4">
              Notre Histoire
            </h2>
            <p class="text-lg text-gray-300 leading-relaxed mb-4">
              "Les Petits Pandas" a été fondé en 2022 par une équipe de passionnés
              d'éducation de la petite enfance. Notre mission est de créer un
              environnement chaleureux et stimulant où chaque enfant se sent
              aimé et en sécurité.
            </p>
            <p class="text-lg text-gray-300 leading-relaxed">
              Nous croyons fermement que les premières années sont les plus
              importantes pour le développement. C'est pourquoi nous mettons l'accent
              sur le jeu libre, les activités créatives et l'apprentissage par la
              découverte.
            </p>
          </div>
          <div class="md:order-2">
            <img src="/images/im3.jpeg" alt="L'histoire des petits pandas" class="w-full h-80 object-cover rounded-xl shadow-xl transition-transform duration-500 hover:scale-105">
          </div>
        </div>
      </section>

      <section class="py-20 animate-fade-in-up animation-delay-1000">
        <div class="container mx-auto px-6 text-center">
          <h2 class="text-4xl font-bold text-shadow-glow mb-12">
            Rencontrez notre Équipe
          </h2>
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            <div class="bg-gray-800 p-6 rounded-lg shadow-xl">
              <img src="/images/im4.jpeg" alt="Membre de l'équipe" class="w-32 h-32 mx-auto rounded-full object-cover mb-4">
              <h3 class="font-semibold text-lg text-white">
                Prénom Nom
              </h3>
              <p class="text-sm text-green-400">
                Fondatrice et Directrice
              </p>
            </div>
            <div class="bg-gray-800 p-6 rounded-lg shadow-xl">
              <img src="/images/im5.jpeg" alt="Membre de l'équipe" class="w-32 h-32 mx-auto rounded-full object-cover mb-4">
              <h3 class="font-semibold text-lg text-white">
                Prénom Nom
              </h3>
              <p class="text-sm text-teal-400">
                Éducatrice en chef
              </p>
            </div>
            <div class="bg-gray-800 p-6 rounded-lg shadow-xl">
              <img src="/images/im1.jpeg" alt="Membre de l'équipe" class="w-32 h-32 mx-auto rounded-full object-cover mb-4">
              <h3 class="font-semibold text-lg text-white">
                Prénom Nom
              </h3>
              <p class="text-sm text-blue-400">
                Spécialiste en développement
              </p>
            </div>
            <div class="bg-gray-800 p-6 rounded-lg shadow-xl">
              <img src="/images/im2.jpeg" alt="Membre de l'équipe" class="w-32 h-32 mx-auto rounded-full object-cover mb-4">
              <h3 class="font-semibold text-lg text-white">
                Prénom Nom
              </h3>
              <p class="text-sm text-gray-400">
                Responsable des activités
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
  title: 'À Propos de Nous - Les Petits Pandas',
  meta: [
    { name: 'description', content: 'Découvrez l\'histoire et l\'équipe passionnée de la garderie Les Petits Pandas. Notre mission est de fournir un environnement sûr et stimulant pour les enfants.' }
  ]
})

// Assurez-vous d'avoir les styles dans un fichier global ou de les copier ici
</script>

<style scoped>
.animation-delay-500 { animation-delay: 0.5s; }
.animation-delay-1000 { animation-delay: 1s; }
</style>
