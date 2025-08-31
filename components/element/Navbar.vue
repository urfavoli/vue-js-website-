<template>
  <header
    class="absolute inset-x-0 top-0 z-50 py-6"
    :class="{ 'backdrop-blur-sm bg-gray-900/40': navIsOpen }"
  >
    <div
      class="w-full px-5 sm:px-10 md:px-12 lg:px-5 mx-auto max-w-7xl"
    >
      <nav class="w-full flex justify-between gap-6 relative">
        <div class="min-w-max inline-flex relative z-20">
          <nuxt-link
            to="/"
            class="relative flex items-center gap-3 font-semibold text-white text-lg transition-all duration-300 ease-linear hover:text-emerald-400"
          >
            <span
              class="flex transition-all duration-300 ease-in-out glow-on-hover"
            >
              <span class="w-3 h-6 rounded-l-full flex bg-emerald-600"></span>
              <span class="w-3 h-6 rounded-r-full flex bg-teal-400 mt-1.5"></span>
            </span>
            <div class="inline-flex">petits pandas</div>
          </nuxt-link>
        </div>

        <div
          aria-hidden="true"
          class="fixed inset-0 lg:hidden backdrop-filter backdrop-blur-xl bg-neutral-800/40"
          :class="navIsOpen ? 'flex' : 'hidden'"
          @click="toggleNavBar"
        ></div>

        <div
          class="absolute lg:relative w-full flex flex-col lg:flex-row gap-y-6 lg:justify-between lg:items-center bg-gray-800 lg:bg-transparent"
          :class="
            navIsOpen
              ? 'translate-y-0 visible opacity-100 top-[calc(100%+1.5rem)]'
              : 'translate-y-10 invisible opacity-0 lg:visible lg:opacity-100 lg:translate-y-0 lg:top-0'
          "
        >
          <ul
            class="px-6 pt-6 flex flex-col lg:flex-row gap-y-4 gap-x-3 text-lg text-white w-full lg:justify-center lg:items-center"
          >
            <li v-for="navItem in navItems" :key="navItem.id">
              <nuxt-link
                :to="navItem.href"
                class="block w-full duration-300 font-medium ease-linear py-3 transition-all glow-on-hover"
                @click="closeNavBar"
              >
                <span class="relative z-10">{{ navItem.text }}</span>
              </nuxt-link>
            </li>
          </ul>

          <div
            class="lg:min-w-max flex items-center sm:w-max w-full pb-6 lg:pb-0 px-6 lg:px-0"
          >
            <nuxt-link
              to="#"
              class="glow-on-hover-cta relative z-10 flex justify-center items-center w-full sm:w-max px-6 h-12 rounded-full border border-green-400 transition duration-300 ease-in-out"
              @click="closeNavBar"
            >
              <span class="relative z-10 text-white font-semibold">
                Commencer ici
              </span>
            </nuxt-link>
          </div>
        </div>

        <div class="min-w-max flex items-center gap-x-3 z-20">
          <ui-toggle-theme />
          <button
            aria-label="toggle navbar"
            @click="toggleNavBar"
            class="lg:hidden w-7 h-auto flex flex-col relative bg-transparent"
          >
            <span
              class="bg-white w-6 h-0.5 rounded-full transition-all duration-300 ease-linear"
              :class="navIsOpen ? 'translate-y-1.5 rotate-45' : ''"
            ></span>
            <span
              class="bg-white w-6 h-0.5 rounded-full mt-1 transition-all duration-300 ease-linear"
              :class="navIsOpen ? 'opacity-0 scale-x-0' : ''"
            ></span>
            <span
              class="bg-white w-6 h-0.5 rounded-full mt-1 transition-all duration-300 ease-linear"
              :class="navIsOpen ? '-translate-y-1.5 -rotate-45' : ''"
            ></span>
          </button>
        </div>
      </nav>
    </div>
  </header>
</template>

<script setup>
//
// === DOCUMENTATION: JAVASCRIPT LOGIC ===
//

// State management for the mobile navigation menu.
const navIsOpen = useState("navIsOpen", () => false);

// Data for navigation links.
const navItems = [
  {
    id: 1,
    text: "Home",
    href: "/",
  },
  {
    id: 2,
    text: "Services",
    href: "/services", // Example of a different page
  },
  {
    id: 3,
    text: "About us",
    href: "/about", // Example of a different page
  },
  {
    id: 4,
    text: "Features",
    href: "/features", // Example of a different page
  },
];

// Function to toggle the mobile navigation menu.
function toggleNavBar() {
  navIsOpen.value = !navIsOpen.value;
  // Prevents scrolling when the menu is open.
  if (navIsOpen.value) {
    document.body.classList.add("overflow-hidden");
  } else {
    document.body.classList.remove("overflow-hidden");
  }
}

// Function to close the navigation menu, useful for clicking on a link.
function closeNavBar() {
  navIsOpen.value = false;
  document.body.classList.remove("overflow-hidden");
}
</script>

<style scoped>
/*
  ==========================================
  DOCUMENTATION: CSS STYLING & ANIMATIONS
  ==========================================
*/

/* --- 1. Global Navbar Styles --- */
/* Ensures the navbar is transparent by default but gains a backdrop on mobile menu open */
header {
  transition: all 0.3s ease-in-out;
}

/* --- 2. Glowing Effect for Links and CTA --- */
/*
  This class creates a subtle glow on hover for text links.
  It's applied to the logo and each navigation item.
*/
.glow-on-hover {
  position: relative;
  transition: all 0.3s ease-in-out;
  color: #fff;
}
.glow-on-hover:hover {
  text-shadow: 0 0 8px rgba(0, 255, 200, 0.6), 0 0 15px rgba(0, 255, 150, 0.4);
  transform: scale(1.05); /* Slight scaling for a more dynamic feel */
  color: #00ffc8;
}

/*
  This class is for the main CTA button. It has a more pronounced glow.
*/
.glow-on-hover-cta {
  box-shadow: 0 0 10px rgba(0, 255, 200, 0.4);
}
.glow-on-hover-cta:hover {
  transform: translateY(-2px) scale(1.05);
  box-shadow: 0 0 15px rgba(0, 255, 200, 0.7),
    0 0 25px rgba(0, 255, 150, 0.5), 0 0 40px rgba(0, 200, 255, 0.3);
}

/* --- 3. Hover Effect for CTA Button --- */
/*
  The `::after` pseudo-element creates a dynamic fill effect on hover,
  giving the button a liquid-like animation.
*/
.glow-on-hover-cta::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 9999px; /* This creates the full circle shape */
  background-color: rgba(0, 255, 200, 0.2);
  transform: scale(0);
  transition: transform 0.3s ease-in-out;
  z-index: 0;
}

.glow-on-hover-cta:hover::after {
  transform: scale(1);
}

/* --- 4. Mobile Menu Transition --- */
/*
  This CSS ensures the hamburger icon transforms smoothly into an "X"
  when the menu is toggled.
*/
button.lg\:hidden span {
  transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
}
button.lg\:hidden span:nth-child(2) {
  margin-top: 4px; /* Adjust spacing to make it look better */
}
button.lg\:hidden span:nth-child(3) {
  margin-top: 4px; /* Adjust spacing to make it look better */
}
</style>