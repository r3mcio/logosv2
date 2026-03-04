<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { Menu, X, Phone, ChevronDown } from 'lucide-vue-next';
import { RouterLink } from 'vue-router';

const isOpen = ref(false);
const isOfferOpen = ref(false);
const isOfferMobileOpen = ref(false);
const dropdownRef = ref(null);

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

const closeDropdown = (e) => {
  const el = Array.isArray(dropdownRef.value) ? dropdownRef.value[0] : dropdownRef.value;
  if (el && el.contains && !el.contains(e.target)) {
    isOfferOpen.value = false;
  }
};

onMounted(() => document.addEventListener('click', closeDropdown));
onUnmounted(() => document.removeEventListener('click', closeDropdown));
</script>

<template>
  <nav class="bg-neutral-950/75 backdrop-blur-xl backdrop-saturate-150 border-b border-white/[0.06] sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-20 items-center">
        <div class="flex items-center -ml-4 lg:-ml-6" data-aos="fade-down">
          <RouterLink to="/" class="group">
             <img src="/logobeztla.webp" alt="Logos" class="h-12 md:h-14 w-auto object-contain brightness-0 invert opacity-90 group-hover:opacity-100 transition-opacity" width="200" height="56" />
          </RouterLink>
        </div>
        
        <!-- Desktop Navigation -->
        <div class="hidden md:flex items-center space-x-8">
          <template v-for="item in navigation" :key="item.name">
            <!-- Item with dropdown -->
            <div v-if="item.children" class="relative" ref="dropdownRef" @mouseenter="isOfferOpen = true" @mouseleave="isOfferOpen = false">
              <button
                @click="isOfferOpen = !isOfferOpen"
                class="text-neutral-400 hover:text-brand-500 font-medium transition-colors inline-flex items-center gap-1"
              >
                {{ item.name }}
                <ChevronDown class="w-3.5 h-3.5 transition-transform duration-200" :class="isOfferOpen ? 'rotate-180' : ''" />
              </button>

              <!-- Dropdown menu -->
              <Transition
                enter-active-class="transition duration-200 ease-out"
                enter-from-class="opacity-0 -translate-y-2"
                enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition duration-150 ease-in"
                leave-from-class="opacity-100 translate-y-0"
                leave-to-class="opacity-0 -translate-y-2"
              >
                <div
                  v-show="isOfferOpen"
                  class="absolute top-full left-1/2 -translate-x-1/2 pt-2 w-52"
                >
                  <div class="bg-neutral-900/95 backdrop-blur-xl border border-neutral-800 rounded-xl shadow-2xl shadow-black/40 overflow-hidden py-1.5">
                    <RouterLink
                      v-for="child in item.children"
                      :key="child.name"
                      :to="child.href"
                      class="block px-4 py-2.5 text-sm text-neutral-400 hover:text-brand-400 hover:bg-brand-950/50 transition-all duration-200 font-medium"
                    >
                      {{ child.name }}
                    </RouterLink>
                  </div>
                </div>
              </Transition>
            </div>

            <!-- Regular item -->
            <RouterLink v-else :to="item.href" class="text-neutral-400 hover:text-brand-500 font-medium transition-colors">
              {{ item.name }}
            </RouterLink>
          </template>
        </div>

        <div class="flex items-center gap-4">
            <a href="tel:+48500277836" class="hidden md:flex items-center gap-2 text-neutral-300 hover:text-brand-500 font-bold transition-colors">
            <Phone class="w-4 h-4" />
            +48 500 277 836
            </a>
            
             <!-- Mobile menu button -->
            <div class="-mr-2 flex items-center md:hidden">
            <button @click="isOpen = !isOpen" class="inline-flex items-center justify-center p-2 rounded-md text-neutral-300 hover:text-brand-500 hover:bg-neutral-900 focus:outline-none transition-colors">
                <Menu v-if="!isOpen" class="block h-6 w-6" aria-hidden="true" />
                <X v-else class="block h-6 w-6" aria-hidden="true" />
            </button>
            </div>
        </div>
      </div>
    </div>
     <!-- Mobile menu -->
    <div v-show="isOpen" class="md:hidden bg-neutral-950/95 backdrop-blur-md border-t border-neutral-800 absolute w-full shadow-xl">
      <div class="pt-2 pb-4 space-y-1">
        <template v-for="item in navigation" :key="item.name">
          <!-- Item with children (Oferta) -->
          <div v-if="item.children">
            <button
              @click="isOfferMobileOpen = !isOfferMobileOpen"
              class="w-full text-left pl-3 pr-4 py-3 border-l-4 border-transparent text-base font-medium text-neutral-400 hover:bg-neutral-900 hover:border-brand-500 hover:text-brand-400 transition-all flex items-center justify-between"
            >
              {{ item.name }}
              <ChevronDown class="w-4 h-4 transition-transform duration-200" :class="isOfferMobileOpen ? 'rotate-180' : ''" />
            </button>
            <!-- Sub-items -->
            <div v-show="isOfferMobileOpen" class="bg-neutral-900/50">
              <RouterLink
                v-for="child in item.children"
                :key="child.name"
                :to="child.href"
                @click="isOpen = false; isOfferMobileOpen = false"
                class="block pl-8 pr-4 py-2.5 border-l-4 border-transparent text-sm font-medium text-neutral-500 hover:bg-neutral-900 hover:border-brand-600 hover:text-brand-400 transition-all"
              >
                {{ child.name }}
              </RouterLink>
            </div>
          </div>

          <!-- Regular item -->
          <RouterLink v-else :to="item.href" @click="isOpen = false" class="block pl-3 pr-4 py-3 border-l-4 border-transparent text-base font-medium text-neutral-400 hover:bg-neutral-900 hover:border-brand-500 hover:text-brand-400 transition-all">
            {{ item.name }}
          </RouterLink>
        </template>
      </div>
    </div>
  </nav>
</template>
