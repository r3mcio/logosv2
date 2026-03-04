<script setup>
import { Phone, Truck, Scale, BadgeCheck } from 'lucide-vue-next';
</script>

<template>
  <section class="relative bg-neutral-950 border-b border-neutral-800 overflow-hidden h-auto lg:min-h-[75vh] flex flex-col lg:block">
    
    <!-- Image half (right side on desktop, top on mobile) -->
    <div class="order-first lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2 h-80 sm:h-96 lg:h-full w-full bg-neutral-900 relative z-0">
       <img class="absolute inset-0 w-full h-full object-cover opacity-80" src="/wmremove-transformed.webp" alt="Skup bydła i transport zwierząt Szczecinek - Bydło-Trans" fetchpriority="high" decoding="async" width="1200" height="800">
       
       <!-- Blur edge between image and content on desktop -->
       <div class="hidden lg:block absolute inset-y-0 left-0 w-40 -translate-x-1/2 z-10 backdrop-blur-2xl [mask-image:linear-gradient(to_right,transparent,black,transparent)] pointer-events-none"></div>
       
       <!-- Bottom fade on mobile -->
       <div class="block lg:hidden absolute inset-x-0 bottom-0 h-24 bg-gradient-to-t from-neutral-950 via-neutral-950/80 to-transparent z-10 pointer-events-none"></div>

       <!-- Region card -->
       <div class="absolute bottom-4 left-4 lg:bottom-8 lg:left-8 z-30 bg-neutral-900/95 backdrop-blur-md p-4 rounded-xl shadow-xl border border-neutral-700/60 max-w-[280px] lg:max-w-xs transform hover:scale-105 transition-transform duration-300">
         <div class="flex items-start gap-3 lg:gap-4">
           <div class="p-2 bg-brand-900/50 rounded-lg text-brand-500 shrink-0">
             <Truck class="w-5 h-5 lg:w-6 lg:h-6" />
           </div>
           <div>
             <p class="text-[10px] text-neutral-500 font-bold uppercase tracking-wider mb-0.5">Region działania</p>
             <p class="font-bold text-white text-sm lg:text-base leading-tight">Zachodniopomorskie + Cała Polska</p>
           </div>
         </div>
       </div>
    </div>

    <!-- Decorative background element -->
    <div class="absolute left-0 top-1/2 -translate-y-1/2 -translate-x-1/2 opacity-[0.03] pointer-events-none hidden lg:block z-0">
        <Truck class="w-[800px] h-[800px] text-white" />
    </div>

    <!-- Content area -->
    <div class="order-last lg:order-none w-full h-full relative z-20 pointer-events-none flex flex-col justify-center">
      
      <div class="w-full lg:w-1/2 px-4 py-8 lg:py-16 xl:py-20 flex flex-col lg:flex-row items-start justify-start gap-8 lg:gap-12 lg:px-0 lg:pl-[6%] xl:pl-[8%] 2xl:pl-[10%] pointer-events-auto bg-neutral-950 lg:bg-transparent">
          
          <!-- Stats sidebar -->
          <div class="flex flex-row lg:flex-col gap-6 lg:gap-8 border-t lg:border-t-0 lg:border-l border-neutral-800 lg:border-neutral-700 pt-6 lg:pt-2 lg:pl-4 z-20 w-full lg:w-auto justify-between lg:justify-start shrink-0 order-last lg:order-first">
             <div class="flex flex-col items-center lg:items-start">
                <span class="text-lg lg:text-xl font-black text-white tracking-tighter">18+</span>
                <span class="text-[10px] font-bold uppercase tracking-wider text-neutral-500 mt-0.5">Lat na rynku</span>
             </div>
             <div class="flex flex-col items-center lg:items-start">
                <span class="text-lg lg:text-xl font-black text-white tracking-tighter">100%</span>
                <span class="text-[10px] font-bold uppercase tracking-wider text-neutral-500 mt-0.5">Polski kapitał</span>
             </div>
             <div class="flex flex-col items-center lg:items-start">
                <span class="text-lg lg:text-xl font-black text-white tracking-tighter">24H</span>
                <span class="text-[10px] font-bold uppercase tracking-wider text-neutral-500 mt-0.5">Czas dojazdu</span>
             </div>
          </div>

          <!-- Main content -->
          <div class="flex flex-col justify-start text-left items-start relative z-10 flex-grow max-w-xl lg:max-w-2xl">
            
            <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-950 text-brand-400 text-xs font-bold mb-4 lg:mb-6 border border-brand-900 shadow-sm">
              <span class="w-2 h-2 rounded-full bg-brand-600 animate-pulse"></span>
              DZIAŁAMY W CAŁYM REGIONIE
            </div>

            <h1 class="text-3xl sm:text-4xl lg:text-[2.75rem] xl:text-5xl tracking-tight font-black text-white mb-4 lg:mb-5 leading-tight">
              <span class="block text-white">Profesjonalny</span>
              <span class="block text-brand-500">Skup Bydła.</span>
            </h1>

            <p class="text-sm sm:text-base lg:text-lg text-neutral-400 leading-relaxed font-medium mb-6 lg:mb-8 lg:max-w-lg">
              <strong class="text-white">Gotówka od ręki</strong>, szybki odbiór (2-7 dni) i pomoc w załadunku. Zaufaj firmie Marcina Kiedla z ponad 18-letnim doświadczeniem.
            </p>
            
            <!-- Features row -->
            <div class="flex flex-wrap gap-x-8 gap-y-3 mb-8 text-neutral-300">
               <div class="flex items-center gap-2">
                 <Truck class="w-4 h-4 text-brand-500 shrink-0" />
                 <span class="text-sm font-bold">Własny transport</span>
               </div>
               <div class="flex items-center gap-2">
                 <Scale class="w-4 h-4 text-brand-500 shrink-0" />
                 <span class="text-sm font-bold">Uczciwa waga</span>
               </div>
               <div class="flex items-center gap-2">
                 <BadgeCheck class="w-4 h-4 text-brand-500 shrink-0" />
                 <span class="text-sm font-bold">Płatność od ręki</span>
               </div>
            </div>

            <!-- Buttons -->
            <div class="w-full sm:w-auto overflow-hidden rounded-xl bg-neutral-900 border border-neutral-800 shadow-2xl relative group">
              <div class="absolute inset-0 bg-brand-500/10 opacity-0 group-hover:opacity-100 transition-opacity"></div>
              <div class="px-6 py-4 flex items-center justify-between gap-6 border-b border-neutral-800/50">
                <div>
                  <p class="text-[10px] font-bold uppercase tracking-wider text-neutral-500 mb-1">Darmowa wycena i dojazd</p>
                  <p class="text-white font-medium text-sm">Zadzwoń po ofertę</p>
                </div>
              </div>
              <div class="bg-neutral-900/50 p-4">
              <a href="tel:+48500277836" class="inline-flex items-center justify-center px-6 py-3 text-sm font-bold rounded-xl text-white bg-brand-600 hover:bg-brand-700 transition-all shadow-lg hover:shadow-brand-600/30 active:scale-95 w-full">
                <Phone class="w-4 h-4 mr-2" />
                500 277 836
              </a>
              </div>
              <RouterLink to="/oferta/skup-bydla" class="inline-flex items-center justify-center px-6 py-3 border border-neutral-700 text-sm font-bold rounded-xl text-neutral-300 bg-neutral-900 hover:bg-neutral-800 transition-all shadow-sm hover:border-brand-800 active:bg-neutral-800 w-full mt-3">
                Sprawdź ofertę
              </RouterLink>
            </div>
          </div>
      </div>
    </div>
  </section>
</template>