<template>
  <footer class="pt-16 md:pt-20 bg-gray-900 text-white">
    <div class="px-5 sm:px-10 md:px-12 lg:px-5 max-w-7xl mx-auto">
      <div
        class="w-full grid grid-cols-2 lg:grid-cols-4 gap-8 pb-4 border-b border-gray-700 text-gray-300"
      >
        <div class="flex">
          <nuxt-link to="/" class="flex items-center gap-3">
            <span
              class="flex transition-all duration-300 ease-in-out glow-on-hover"
            >
              <span class="w-3 h-6 rounded-l-full flex bg-emerald-600"></span>
              <span class="w-3 h-6 rounded-r-full flex bg-teal-400 mt-1.5"></span>
            </span>
            <div class="inline-flex font-semibold text-white">petits pandas</div>
          </nuxt-link>
        </div>
        <div class="flex items-center space-x-2">
          <span class="i-carbon-location flex text-xl glow-on-hover"></span>
          <span>Cad , Saint Jerome</span>
        </div>
        <div class="flex items-center space-x-2">
          <span class="i-carbon-phone flex text-xl glow-on-hover"></span>
          <span>+1 ...............</span>
        </div>
        <div class="flex items-center space-x-2">
          <span class="i-carbon-email flex text-2xl glow-on-hover"></span>
          <span>......@gmail.com</span>
        </div>
      </div>

      <nav
        class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-y-10 gap-8 py-10 text-gray-300"
      >
        <div v-for="footerItem in footerLinks" :key="footerItem.id" class="space-y-5">
          <h1 class="text-lg text-white font-semibold">
            {{ footerItem.title }}
          </h1>
          <ul class="space-y-3">
            <li v-for="item in footerItem.items" :key="item.id">
              <nuxt-link
                :to="item.link"
                class="hover:text-emerald-500 duration-200 transition-all glow-on-hover"
              >
                {{ item.label }}
              </nuxt-link>
            </li>
          </ul>
        </div>

        <div class="space-y-5 col-span-2 md:col-span-3 lg:col-span-1">
          <h1 class="text-lg text-white font-semibold">
            Inscrivez-vous à notre newsletter
          </h1>
          <p class="max-w-xl">
            Recevez nos dernières actualités et offres spéciales directement
            dans votre boîte de réception.
          </p>
          <form class="grid w-full relative max-w-xl">
            <div class="flex flex-col gap-3 w-full relative">
              <input
                type="email"
                class="w-full outline-none px-3 py-3 rounded-full bg-gray-800 border border-gray-700 text-white placeholder-gray-500"
                placeholder="johndoe@gmail.com"
              />
              <button
                type="submit"
                class="glow-on-hover-cta w-full py-3 sm:py-0 sm:w-max sm:absolute sm:right-1 sm:inset-y-1 px-4 text-sm flex sm:items-center justify-center outline-none bg-emerald-600 text-white rounded-3xl relative overflow-hidden"
              >
                <span class="relative z-10 font-semibold">
                  S'inscrire
                </span>
              </button>
            </div>
          </form>
        </div>
      </nav>

      <div
        class="w-full flex flex-col md:flex-row gap-4 items-center sm:justify-between py-3 border-t border-gray-700 text-gray-300"
      >
        <div class="flex sm:min-w-max">
          <p class="text-center sm:text-left">
            © 2025 Les Petits Pandas. Tous droits réservés.
          </p>
        </div>
        <div class="flex justify-center sm:justify-end w-full gap-3">
          <nuxt-link to="#" aria-label="social link" class="glow-on-hover text-2xl flex">
            <span class="i-carbon-logo-facebook"></span>
          </nuxt-link>
          <nuxt-link to="#" aria-label="social link" class="glow-on-hover text-2xl flex">
            <span class="i-carbon-logo-linkedin"></span>
          </nuxt-link>
          <nuxt-link to="#" aria-label="social link" class="glow-on-hover text-2xl flex">
            <span class="i-carbon-logo-twitter"></span>
          </nuxt-link>
          <nuxt-link to="#" aria-label="social link" class="glow-on-hover text-2xl flex">
            <span class="i-carbon-logo-instagram"></span>
          </nuxt-link>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
//
// === DOCUMENTATION: DONNÉES ET LOGIQUE ===
//

// Données pour les liens du pied de page.
const footerLinks = [
  {
    id: 1,
    title: "Navigation",
    items: [
      { id: 1, label: 'Accueil', link: '/' },
      { id: 2, label: 'Services', link: '/services' },
      { id: 3, label: 'À propos', link: '/about' },
      { id: 4, label: 'Contact', link: '/contact' },
    ]
  },
  {
    id: 2,
    title: "Services",
    items: [
      { id: 1, label: 'Activités d\'éveil', link: '/services#activities' },
      { id: 2, label: 'Repas bio', link: '/services#meals' },
      { id: 3, label: 'Garderie flexible', link: '/services#flexibility' },
      { id: 4, label: 'Sécurité', link: '/services#safety' },
    ]
  },
  {
    id: 3,
    title: "Support",
    items: [
      { id: 1, label: 'FAQ', link: '/faq' },
      { id: 2, label: 'Politique de confidentialité', link: '/privacy-policy' },
      { id: 3, label: 'Termes & Conditions', link: '/terms' },
      { id: 4, label: 'Aide', link: '/help' },
    ]
  },
];
</script>

<style scoped>
/*
  ==========================================
  DOCUMENTATION CSS : STYLES ET ANIMATIONS
  ==========================================
*/

/*
  La classe 'glow-on-hover' est réutilisée de la page d'accueil
  pour une cohérence visuelle sur les liens.
*/
.glow-on-hover {
  position: relative;
  transition: all 0.3s ease-in-out;
}
.glow-on-hover:hover {
  color: #00ffc8;
  text-shadow: 0 0 8px rgba(0, 255, 200, 0.6), 0 0 15px rgba(0, 255, 150, 0.4);
  transform: translateY(-2px);
}

/*
  La classe 'glow-on-hover-cta' est utilisée pour le bouton de la newsletter
  afin de lui donner la même lueur que les boutons principaux.
*/
.glow-on-hover-cta {
  box-shadow: 0 0 10px rgba(0, 255, 200, 0.4);
}
.glow-on-hover-cta:hover {
  transform: translateY(-2px) scale(1.05);
  box-shadow: 0 0 15px rgba(0, 255, 200, 0.7),
    0 0 25px rgba(0, 255, 150, 0.5), 0 0 40px rgba(0, 200, 255, 0.3);
}

/*
  L'animation du bouton d'inscription pour un effet plus "cool".
  Ceci remplace l'implémentation originale de `un-after`.
*/
.glow-on-hover-cta::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 9999px;
  background-color: rgba(0, 255, 200, 0.2);
  transform: scale(0);
  transition: transform 0.3s ease-in-out;
  z-index: 0;
}

.glow-on-hover-cta:hover::after {
  transform: scale(1.2);
}
</style>