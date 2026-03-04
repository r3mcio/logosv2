<script setup>
import { MapPin, Phone, Mail, ArrowRight, ChevronDown } from 'lucide-vue-next';
import { ref } from 'vue';

const currentYear = new Date().getFullYear();
const isOfferOpen = ref(false);

const navigation = [
  { name: 'Start', href: '/' },
  { name: 'O Nas', href: '/o-nas' },
  {
    name: 'Oferta',
    href: '/oferta/skup-bydla',
    children: [
      { name: 'Skup bydła', href: '/oferta/skup-bydla' },
      { name: 'Sprzedaż bydła', href: '/oferta/sprzedaz-bydla' },
      { name: 'Transport bydła', href: '/oferta/transport-bydla' },
      { name: 'Sprzedaż mięs', href: '/oferta/sprzedaz-mies' },
    ],
  },
  { name: 'Kontakt', href: '/kontakt' },
];
</script>

<template>
  <footer class="w-full font-sans relative z-30 flex flex-col">
    

    <!-- 2. ULTRA-COMPACT FOOTER -->
    <div class="bg-black text-neutral-400 py-8 border-t border-neutral-800 mt-auto">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <!-- Horizontal Layout Container -->
        <div class="flex flex-col lg:flex-row items-center justify-between gap-8 lg:gap-4">
          
          <!-- LEFT: Logo & Location -->
          <div class="flex flex-col items-center lg:items-start gap-2 text-center lg:text-left">
            <RouterLink to="/" class="flex items-center gap-2 group">
              <img src="/logobeztla.webp" alt="Logos" class="h-12 w-auto object-contain brightness-0 invert opacity-90 group-hover:opacity-100 transition-opacity" width="200" height="48" />
            </RouterLink>
            <p class="text-xs text-neutral-600 mt-2 leading-relaxed">
              Logos Marcin Kiedel<br />
              [Ulica]<br />
              78-400 Szczecinek
            </p>
          </div>

          <!-- CENTER: Minimalist Navigation -->
          <nav class="flex flex-wrap justify-center items-center gap-x-6 gap-y-2">
            <template v-for="item in navigation" :key="item.name">
              <!-- Item with dropdown -->
              <div v-if="item.children" class="relative" @mouseenter="isOfferOpen = true" @mouseleave="isOfferOpen = false">
                <button
                  @click="isOfferOpen = !isOfferOpen"
                  class="text-sm font-medium text-neutral-500 hover:text-brand-500 transition-colors inline-flex items-center gap-1"
                >
                  {{ item.name }}
                  <ChevronDown class="w-3.5 h-3.5 transition-transform duration-200" :class="isOfferOpen ? 'rotate-180' : ''" />
                </button>

                <!-- Dropdown menu (opens upwards) -->
                <Transition
                  enter-active-class="transition duration-200 ease-out"
                  enter-from-class="opacity-0 translate-y-2"
                  enter-to-class="opacity-100 translate-y-0"
                  leave-active-class="transition duration-150 ease-in"
                  leave-from-class="opacity-100 translate-y-0"
                  leave-to-class="opacity-0 translate-y-2"
                >
                  <div
                    v-show="isOfferOpen"
                    class="absolute bottom-full left-1/2 -translate-x-1/2 pb-2 w-48 z-50"
                  >
                    <div class="bg-neutral-900/95 backdrop-blur-xl border border-neutral-800 rounded-xl shadow-2xl shadow-black/40 overflow-hidden py-1.5 flex flex-col items-center">
                      <RouterLink
                        v-for="child in item.children"
                        :key="child.name"
                        :to="child.href"
                        class="block w-full px-4 py-2.5 text-sm text-neutral-400 hover:text-brand-400 hover:bg-brand-950/50 transition-all duration-200 font-medium text-center"
                      >
                        {{ child.name }}
                      </RouterLink>
                    </div>
                  </div>
                </Transition>
              </div>

              <!-- Regular item -->
              <RouterLink v-else :to="item.href" class="text-sm font-medium text-neutral-500 hover:text-brand-500 transition-colors">
                {{ item.name }}
              </RouterLink>
            </template>
          </nav>

          <!-- RIGHT: Contact & Map Link -->
          <div class="flex flex-col items-center lg:items-end gap-2 text-sm">
            <div class="flex flex-col sm:flex-row items-start sm:items-center gap-2 sm:gap-4 mt-1">
              <a href="tel:+48500277836" class="flex items-center gap-2 text-neutral-300 hover:text-brand-500 transition-colors font-bold">
                <Phone class="w-4 h-4 text-brand-500" />
                500 277 836
              </a>
              <span class="text-neutral-700">|</span>
              <a href="mailto:biuro@bydlo-trans.pl" class="flex items-center gap-2 text-neutral-500 hover:text-brand-500 transition-colors">
                <Mail class="w-4 h-4" />
                logos@skup-bydla.pl
              </a>
            </div>
            <a href="#" class="text-xs text-neutral-600 hover:text-brand-500 transition-colors flex items-center gap-1 mt-1">
              <MapPin class="w-3 h-3" />
              Zobacz naszą bazę w Szczecinku
            </a>
          </div>

        </div>

        <!-- Very subtle copyright line -->
        <div class="mt-8 pt-6 border-t border-neutral-800 text-center text-[10px] text-neutral-600 flex flex-col sm:flex-row justify-between items-center gap-4 sm:gap-2">
          <p class="w-full sm:flex-1 text-center sm:text-left">&copy; {{ currentYear }} Logos. Wszelkie prawa zastrzeżone.</p>
          <div class="w-full sm:flex-1 flex justify-center">
            <span class="hover:text-brand-500 transition-colors cursor-default font-medium tracking-wide">Created by - CodeWave</span>
          </div>
          <div class="w-full sm:flex-1 flex justify-center sm:justify-end gap-4 items-center">
            <RouterLink to="/polityka-prywatnosci" class="hover:text-brand-500 transition-colors">Polityka Prywatności</RouterLink>
          </div>
        </div>

      </div>
    </div>

  </footer>
</template>
