<script setup>
import HeroSection from '../components/HeroSection.vue';
import { Truck, Scale, Banknote, Phone, PhoneCall, Clock, Handshake, ArrowRight, Users, Timer, ShieldCheck, MapPin } from 'lucide-vue-next';
</script>

<template>
  <div>
    <HeroSection />
    
    <!-- Quick Features Section (Trust Indicators) -->
    <section class="py-10 md:py-20 bg-neutral-950 border-b border-neutral-800" data-aos="fade-up">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">
        
        <div class="mb-12">
            <h2 class="text-3xl md:text-4xl font-black text-white tracking-tight mb-4">Dlaczego warto nam zaufać?</h2>
            <p class="text-neutral-400 text-lg max-w-2xl">Profesjonalizm i uczciwość to fundamenty naszej pracy.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8" data-aos="fade-up" data-aos-delay="100">
            <!-- Feature 1 -->
            <div class="bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 rounded-xl p-6 border border-brand-800/30 shadow-xl hover:shadow-brand-950/50 hover:-translate-y-1 transition-all group duration-300">
                <div class="flex items-center gap-4 mb-3">
                    <div class="w-12 h-12 bg-brand-950/50 rounded-lg flex items-center justify-center text-brand-500 shrink-0 shadow-sm border border-brand-800/30 group-hover:scale-110 transition-transform">
                    <Truck class="w-6 h-6" />
                    </div>
                    <h3 class="text-lg font-bold text-white leading-tight">Własna flota<br>transportowa</h3>
                </div>
                <p class="text-neutral-400 text-sm leading-relaxed">
                Posiadamy specjalistyczne pojazdy do przewozu żywca. Odbieramy bydło bezpośrednio z Twojego gospodarstwa.
                </p>
            </div>

            <!-- Feature 2 -->
            <div class="bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 rounded-xl p-6 border border-brand-800/30 shadow-xl hover:shadow-brand-950/50 hover:-translate-y-1 transition-all group duration-300">
                <div class="flex items-center gap-4 mb-3">
                    <div class="w-12 h-12 bg-brand-950/50 rounded-lg flex items-center justify-center text-brand-500 shrink-0 shadow-sm border border-brand-800/30 group-hover:scale-110 transition-transform">
                    <Scale class="w-6 h-6" />
                    </div>
                    <h3 class="text-lg font-bold text-white leading-tight">Uczciwa waga<br>elektroniczna</h3>
                </div>
                <p class="text-neutral-400 text-sm leading-relaxed">
                Ważenie odbywa się w Twojej obecności na legalizowanych wagach. Pełna transparentność i wydruk z wagi.
                </p>
            </div>

            <!-- Feature 3 -->
            <div class="bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 rounded-xl p-6 border border-brand-800/30 shadow-xl hover:shadow-brand-950/50 hover:-translate-y-1 transition-all group duration-300">
                <div class="flex items-center gap-4 mb-3">
                    <div class="w-12 h-12 bg-brand-950/50 rounded-lg flex items-center justify-center text-brand-500 shrink-0 shadow-sm border border-brand-800/30 group-hover:scale-110 transition-transform">
                    <Banknote class="w-6 h-6" />
                    </div>
                    <h3 class="text-lg font-bold text-white leading-tight">Płatność<br>od ręki</h3>
                </div>
                <p class="text-neutral-400 text-sm leading-relaxed">
                Płacimy natychmiast po zważeniu i ustaleniu ceny. Gotówka lub szybki przelew na życzenie rolnika.
                </p>
            </div>
        </div>
      </div>
    </section>

    <!-- Jak to działa? — 3 step process -->
    <section class="py-16 md:py-24 bg-black border-y border-neutral-800 overflow-hidden relative" data-aos="fade-up">
      <div class="absolute inset-0 opacity-[0.04] bg-[url('https://www.transparenttextures.com/patterns/cubes.png')]" style="background-color: rgb(220, 38, 38); background-blend-mode: multiply;"></div>
      <div class="max-w-7xl mx-auto px-6 lg:px-8">
        
        <div class="text-center mb-16">
          <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-950 text-brand-400 text-xs font-bold mb-4 border border-brand-900 shadow-sm">
            <span class="w-2 h-2 rounded-full bg-brand-600 animate-pulse"></span>
            PROSTY PROCES
          </div>
          <h2 class="text-3xl md:text-4xl font-black text-white tracking-tight mb-4">Jak to działa?</h2>
          <p class="text-neutral-400 text-lg max-w-2xl mx-auto">Cały proces od kontaktu do płatności trwa zaledwie kilka godzin. Zero biurokracji, zero czekania.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 lg:gap-12 relative">
          
          <!-- Connecting line (desktop only) -->
          <div class="hidden md:block absolute top-16 left-[20%] right-[20%] h-0.5 bg-gradient-to-r from-brand-800 via-brand-500 to-brand-800 z-0"></div>

          <!-- Step 1 -->
          <div class="relative z-10 text-center group" data-aos="fade-up" data-aos-delay="0">
            <div class="w-32 h-32 mx-auto mb-6 bg-neutral-800 rounded-2xl shadow-lg border border-neutral-700 flex items-center justify-center group-hover:shadow-xl group-hover:border-brand-800 transition-all duration-300 group-hover:-translate-y-1">
              <div class="relative">
                <PhoneCall class="w-12 h-12 text-brand-500" />
                <span class="absolute -top-2 -right-3 w-7 h-7 bg-brand-600 text-white text-sm font-black rounded-full flex items-center justify-center shadow-md">1</span>
              </div>
            </div>
            <h3 class="text-xl font-bold text-white mb-2">Zadzwoń do nas</h3>
            <p class="text-neutral-400 text-sm leading-relaxed max-w-xs mx-auto">Zadzwoń i podaj ile sztuk bydła chcesz sprzedać. Ustalamy termin odbioru — nawet na ten sam dzień.</p>
          </div>

          <!-- Step 2 -->
          <div class="relative z-10 text-center group" data-aos="fade-up" data-aos-delay="150">
            <div class="w-32 h-32 mx-auto mb-6 bg-neutral-800 rounded-2xl shadow-lg border border-neutral-700 flex items-center justify-center group-hover:shadow-xl group-hover:border-brand-800 transition-all duration-300 group-hover:-translate-y-1">
              <div class="relative">
                <Truck class="w-12 h-12 text-brand-500" />
                <span class="absolute -top-2 -right-3 w-7 h-7 bg-brand-600 text-white text-sm font-black rounded-full flex items-center justify-center shadow-md">2</span>
              </div>
            </div>
            <h3 class="text-xl font-bold text-white mb-2">Przyjeżdżamy i ważymy</h3>
            <p class="text-neutral-400 text-sm leading-relaxed max-w-xs mx-auto">Nasz transport przyjeżdża na miejsce. Ważymy bydło na legalizowanej wadze elektronicznej w Twojej obecności.</p>
          </div>

          <!-- Step 3 -->
          <div class="relative z-10 text-center group" data-aos="fade-up" data-aos-delay="300">
            <div class="w-32 h-32 mx-auto mb-6 bg-neutral-800 rounded-2xl shadow-lg border border-neutral-700 flex items-center justify-center group-hover:shadow-xl group-hover:border-brand-800 transition-all duration-300 group-hover:-translate-y-1">
              <div class="relative">
                <Handshake class="w-12 h-12 text-brand-500" />
                <span class="absolute -top-2 -right-3 w-7 h-7 bg-brand-600 text-white text-sm font-black rounded-full flex items-center justify-center shadow-md">3</span>
              </div>
            </div>
            <h3 class="text-xl font-bold text-white mb-2">Płacimy gotówką</h3>
            <p class="text-neutral-400 text-sm leading-relaxed max-w-xs mx-auto">Natychmiast po ustaleniu ceny płacimy gotówką do ręki lub przelewem. Szybko, uczciwie i bez komplikacji.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- O firmie — dark CTA section -->
    <section class="relative py-20 md:py-28 bg-black overflow-hidden" data-aos="fade-up">
      <!-- Background pattern -->
      <div class="absolute inset-0 opacity-5 bg-[url('https://www.transparenttextures.com/patterns/cubes.png')]"></div>
      <!-- Decorative gradient -->
      <div class="absolute inset-0 bg-gradient-to-br from-brand-950/50 via-transparent to-black"></div>
      
      <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 items-center">
          
          <!-- Text content -->
          <div data-aos="fade-right">
            <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-950/50 text-brand-400 text-xs font-bold mb-6 border border-brand-900/30">
              <ShieldCheck class="w-3.5 h-3.5" />
              ZAUFAJ DOŚWIADCZENIU
            </div>
            <h2 class="text-3xl md:text-4xl font-black text-white tracking-tight mb-6 leading-tight">
              Firma z <span class="text-brand-500">tradycją</span> i<br>szacunkiem do rolnika.
            </h2>
            <p class="text-neutral-400 text-base md:text-lg leading-relaxed mb-6">
              Nazywam się <strong class="text-white">Marcin Kiedel</strong> i od ponad 18 lat prowadzę firmę Logos. Przez ten czas zbudowałem relacje z setkami rolników z całego województwa zachodniopomorskiego.
            </p>
            <p class="text-neutral-400 text-base md:text-lg leading-relaxed mb-8">
              Szanuję ciężką pracę rolnika — dlatego stawiam na <strong class="text-white">uczciwość, terminowość</strong> i <strong class="text-white">rzetelne warunki</strong>. Każda transakcja to moje słowo honoru.
            </p>
            <RouterLink to="/o-nas" class="inline-flex items-center gap-2 px-6 py-3 text-sm font-bold rounded-xl text-white bg-brand-600 hover:bg-brand-700 transition-all shadow-lg hover:shadow-brand-600/20 active:scale-95 group">
              Poznaj naszą historię
              <ArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
            </RouterLink>
          </div>

          <!-- Image / visual -->
          <div class="relative" data-aos="fade-left" data-aos-delay="200">
            <div class="relative rounded-2xl overflow-hidden shadow-2xl border border-neutral-800">
              <img src="/wmremove-transformed.webp" alt="Transport bydła - firma Logos" class="w-full h-80 lg:h-96 object-cover" loading="lazy" decoding="async" width="800" height="384" />
              <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent"></div>
              <!-- Floating badge -->
              <div class="absolute bottom-4 left-4 right-4 flex justify-between items-end">
                <div class="bg-neutral-900/95 backdrop-blur-md px-4 py-2.5 rounded-lg shadow-lg border border-neutral-700">
                  <p class="text-xs text-neutral-500 font-bold uppercase tracking-wider">Doświadczenie</p>
                  <p class="text-xl font-black text-white">18+ lat</p>
                </div>
                <div class="bg-neutral-900/95 backdrop-blur-md px-4 py-2.5 rounded-lg shadow-lg border border-neutral-700">
                  <p class="text-xs text-neutral-500 font-bold uppercase tracking-wider">Region</p>
                  <p class="text-xl font-black text-white">Cała Polska</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Liczby mówią same — stats section -->
    <section class="py-16 md:py-20 bg-neutral-950 border-b border-neutral-800" data-aos="fade-up">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">
        
        <div class="text-center mb-14">
          <h2 class="text-3xl md:text-4xl font-black text-white tracking-tight mb-4">Liczby mówią same</h2>
          <p class="text-neutral-400 text-lg max-w-2xl mx-auto">Nasze wyniki to efekt lat ciężkiej pracy i zaufania rolników z całego regionu.</p>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-4 gap-6 md:gap-8">
          
          <!-- Stat 1 -->
          <div class="relative bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 rounded-2xl p-6 md:p-8 text-center border border-brand-800/30 hover:border-brand-500/50 hover:shadow-xl hover:shadow-brand-950/50 hover:-translate-y-1 transition-all duration-300 group" data-aos="fade-up" data-aos-delay="0">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-950/50 rounded-xl flex items-center justify-center text-brand-500 group-hover:scale-110 transition-transform">
              <Clock class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-white mb-1">18+</p>
            <p class="text-sm font-semibold text-neutral-500 uppercase tracking-wider">Lat na rynku</p>
          </div>

          <!-- Stat 2 -->
          <div class="relative bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 rounded-2xl p-6 md:p-8 text-center border border-brand-800/30 hover:border-brand-500/50 hover:shadow-xl hover:shadow-brand-950/50 hover:-translate-y-1 transition-all duration-300 group" data-aos="fade-up" data-aos-delay="100">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-950/50 rounded-xl flex items-center justify-center text-brand-500 group-hover:scale-110 transition-transform">
              <Users class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-white mb-1">1000+</p>
            <p class="text-sm font-semibold text-neutral-500 uppercase tracking-wider">Rolników</p>
          </div>

          <!-- Stat 3 -->
          <div class="relative bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 rounded-2xl p-6 md:p-8 text-center border border-brand-800/30 hover:border-brand-500/50 hover:shadow-xl hover:shadow-brand-950/50 hover:-translate-y-1 transition-all duration-300 group" data-aos="fade-up" data-aos-delay="200">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-950/50 rounded-xl flex items-center justify-center text-brand-500 group-hover:scale-110 transition-transform">
              <Timer class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-white mb-1">24h</p>
            <p class="text-sm font-semibold text-neutral-500 uppercase tracking-wider">Czas reakcji</p>
          </div>

          <!-- Stat 4 -->
          <div class="relative bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 rounded-2xl p-6 md:p-8 text-center border border-brand-800/30 hover:border-brand-500/50 hover:shadow-xl hover:shadow-brand-950/50 hover:-translate-y-1 transition-all duration-300 group" data-aos="fade-up" data-aos-delay="300">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-950/50 rounded-xl flex items-center justify-center text-brand-500 group-hover:scale-110 transition-transform">
              <MapPin class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-white mb-1">Cała</p>
            <p class="text-sm font-semibold text-neutral-500 uppercase tracking-wider">Polska</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Zadzwoń teraz — final CTA section -->
    <section class="relative py-16 md:py-20 bg-gradient-to-br from-brand-900 via-brand-950 to-neutral-900 overflow-hidden" data-aos="fade-up">
      <div class="absolute inset-0 opacity-[0.04] bg-[url('https://www.transparenttextures.com/patterns/cubes.png')]" style="background-color: rgb(220, 38, 38); background-blend-mode: multiply;"></div>
      
      <div class="max-w-4xl mx-auto px-6 lg:px-8 relative z-10 text-center border border-brand-800/30 rounded-3xl p-8 md:p-12 shadow-2xl bg-neutral-900/40 backdrop-blur-sm">
        <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-950/80 text-brand-400 text-xs font-bold mb-6 border border-brand-800/50 shadow-sm" data-aos="fade-up">
          <Phone class="w-3.5 h-3.5" />
          SKONTAKTUJ SIĘ Z NAMI
        </div>
        
        <h2 class="text-3xl md:text-5xl font-black text-white tracking-tight mb-6 leading-tight" data-aos="fade-up" data-aos-delay="100">
          Umów się na odbiór<br>
          <span class="text-brand-500">jeszcze dziś.</span>
        </h2>
        
        <p class="text-neutral-400 text-lg max-w-xl mx-auto mb-10 leading-relaxed" data-aos="fade-up" data-aos-delay="200">
          Jeden telefon wystarczy. Podpowiemy Ci najlepsze warunki sprzedaży i umówimy się na wygodny termin odbioru.
        </p>
        
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4 sm:gap-6 pt-4">
          <a href="tel:+48500277836" class="inline-flex items-center justify-center gap-3 px-8 py-4 text-lg font-bold rounded-2xl text-white bg-brand-600 hover:bg-brand-700 transition-all shadow-xl hover:shadow-brand-600/30 active:scale-95 group">
            <Phone class="w-5 h-5 group-hover:rotate-12 transition-transform" />
            +48 500 277 836
          </a>
          <span class="text-neutral-600 text-sm font-medium hidden sm:block">lub</span>
          <RouterLink to="/kontakt" class="inline-flex items-center justify-center gap-2 px-8 py-4 border border-brand-700/50 text-base font-bold rounded-2xl text-neutral-300 bg-brand-900/30 hover:bg-brand-900/50 transition-all shadow-sm hover:border-brand-500 active:bg-brand-800">
            Napisz do nas
            <ArrowRight class="w-4 h-4" />
          </RouterLink>
        </div>

        <!-- Trust micro-badges -->
        <div class="flex flex-wrap justify-center gap-6 mt-10 text-sm text-neutral-500" data-aos="fade-up" data-aos-delay="400">
          <div class="flex items-center gap-1.5">
            <ShieldCheck class="w-4 h-4 text-brand-500" />
            <span class="font-medium">Bez zobowiązań</span>
          </div>
          <div class="flex items-center gap-1.5">
            <Clock class="w-4 h-4 text-brand-500" />
            <span class="font-medium">Odpowiedź w 15 min</span>
          </div>
          <div class="flex items-center gap-1.5">
            <Banknote class="w-4 h-4 text-brand-500" />
            <span class="font-medium">Uczciwe ceny</span>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>
