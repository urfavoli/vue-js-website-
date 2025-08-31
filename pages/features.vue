<template>
  <div class="relative min-h-screen overflow-hidden bg-gray-900 text-white">
    <div
      class="background-animation absolute inset-0 -z-10"
      aria-hidden="true"
    />

    <main class="py-20 lg:py-32">
      <section class="container mx-auto px-6 text-center animate-fade-in-up">
        <h1 class="text-5xl font-extrabold text-shadow-glow mb-4">
          Nos Atouts Uniques
        </h1>
        <p class="text-xl max-w-2xl mx-auto text-gray-400">
          Découvrez ce qui fait de notre garderie un lieu exceptionnel pour vos
          petits.
        </p>
      </section>

      <section class="py-20 animate-fade-in-up animation-delay-500">
        <div class="container mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
          <div class="md:order-1">
            <h2 class="text-4xl font-bold text-shadow-glow mb-4">
              La Sécurité avant tout
            </h2>
            <p class="text-lg text-gray-300 leading-relaxed">
              Nous avons mis en place des protocoles de sécurité rigoureux,
              incluant un système de surveillance vidéo, des accès sécurisés
              et une équipe formée aux premiers secours. Vos enfants sont
              entre de bonnes mains.
            </p>
          </div>
          <div class="md:order-2">
            <img src="/images/im4.jpeg" alt="Sécurité de la garderie" class="w-full h-80 object-cover rounded-xl shadow-xl transition-transform duration-500 hover:scale-105">
          </div>
        </div>
      </section>

      <section class="py-20 animate-fade-in-up animation-delay-1000">
        <div class="container mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
          <div class="md:order-2">
            <h2 class="text-4xl font-bold text-shadow-glow mb-4">
              Suivi Connecté
            </h2>
            <p class="text-lg text-gray-300 leading-relaxed">
              Grâce à notre application mobile, vous pouvez suivre la journée
              de votre enfant en temps réel. Recevez des photos, des rapports
              de repas et des mises à jour sur ses activités.
            </p>
          </div>
          <div class="md:order-1">
            <img src="/images/im5.jpeg" alt="Application de suivi" class="w-full h-80 object-cover rounded-xl shadow-xl transition-transform duration-500 hover:scale-105">
          </div>
        </div>
      </section>

      <section class="py-20 animate-fade-in-up animation-delay-1500">
        <div class="container mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
          <div class="md:order-1">
            <h2 class="text-4xl font-bold text-shadow-glow mb-4">
              Équipements Modernes
            </h2>
            <p class="text-lg text-gray-300 leading-relaxed">
              Notre établissement dispose d'aires de jeux intérieures et
              extérieures à la pointe, de salles d'activités lumineuses et
              d'équipements pédagogiques de qualité, favorisant le jeu et
              l'apprentissage.
            </p>
          </div>
          <div class="md:order-2">
            <img src="/images/im2.jpeg" alt="Équipements modernes" class="w-full h-80 object-cover rounded-xl shadow-xl transition-transform duration-500 hover:scale-105">
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup>
// Métadonnées de la page pour le SEO
useHead({
  title: 'Nos Atouts - Les Petits Pandas',
  meta: [
    { name: 'description', content: 'Découvrez les atouts uniques de notre garderie : sécurité, technologie de suivi, équipements modernes et plus encore pour un environnement optimal.' }
  ]
})

// Assurez-vous d'avoir les styles dans un fichier global ou de les copier ici
</script>

<style scoped>
.animation-delay-500 { animation-delay: 0.5s; }
.animation-delay-1000 { animation-delay: 1s; }
.animation-delay-1500 { animation-delay: 1.5s; }
</style>
