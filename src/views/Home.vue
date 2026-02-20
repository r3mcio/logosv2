<script setup>
import HeroSection from '../components/HeroSection.vue';
import { Truck, Scale, Banknote, Phone, PhoneCall, Clock, Handshake, ArrowRight, Users, Timer, ShieldCheck, MapPin } from 'lucide-vue-next';
</script>

<template>
  <div>
    <HeroSection />
    
    <!-- Quick Features Section (Trust Indicators) -->
    <section class="py-10 md:py-20 bg-white border-b border-slate-100" data-aos="fade-up">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">
        
        <div class="mb-12">
            <h2 class="text-3xl md:text-4xl font-black text-slate-900 tracking-tight mb-4">Dlaczego warto nam zaufać?</h2>
            <p class="text-slate-600 text-lg max-w-2xl">Profesjonalizm i uczciwość to fundamenty naszej pracy.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8" data-aos="fade-up" data-aos-delay="100">
            <!-- Feature 1 -->
            <div class="bg-slate-50 rounded-xl p-6 border border-slate-100 hover:border-brand-200 transition-colors group">
                <div class="flex items-center gap-4 mb-3">
                    <div class="w-12 h-12 bg-white rounded-lg flex items-center justify-center text-brand-600 shrink-0 shadow-sm border border-slate-100 group-hover:scale-105 transition-transform">
                    <Truck class="w-6 h-6" />
                    </div>
                    <h3 class="text-lg font-bold text-slate-900 leading-tight">Własna flota<br>transportowa</h3>
                </div>
                <p class="text-slate-600 text-sm leading-relaxed">
                Posiadamy specjalistyczne pojazdy do przewozu żywca. Odbieramy bydło bezpośrednio z Twojego gospodarstwa.
                </p>
            </div>

            <!-- Feature 2 -->
            <div class="bg-slate-50 rounded-xl p-6 border border-slate-100 hover:border-brand-200 transition-colors group">
                <div class="flex items-center gap-4 mb-3">
                    <div class="w-12 h-12 bg-white rounded-lg flex items-center justify-center text-brand-600 shrink-0 shadow-sm border border-slate-100 group-hover:scale-105 transition-transform">
                    <Scale class="w-6 h-6" />
                    </div>
                    <h3 class="text-lg font-bold text-slate-900 leading-tight">Uczciwa waga<br>elektroniczna</h3>
                </div>
                <p class="text-slate-600 text-sm leading-relaxed">
                Ważenie odbywa się w Twojej obecności na legalizowanych wagach. Pełna transparentność i wydruk z wagi.
                </p>
            </div>

            <!-- Feature 3 -->
            <div class="bg-slate-50 rounded-xl p-6 border border-slate-100 hover:border-brand-200 transition-colors group">
                <div class="flex items-center gap-4 mb-3">
                    <div class="w-12 h-12 bg-white rounded-lg flex items-center justify-center text-brand-600 shrink-0 shadow-sm border border-slate-100 group-hover:scale-105 transition-transform">
                    <Banknote class="w-6 h-6" />
                    </div>
                    <h3 class="text-lg font-bold text-slate-900 leading-tight">Płatność<br>od ręki</h3>
                </div>
                <p class="text-slate-600 text-sm leading-relaxed">
                Płacimy natychmiast po zważeniu i ustaleniu ceny. Gotówka lub szybki przelew na życzenie rolnika.
                </p>
            </div>
        </div>
      </div>
    </section>

    <!-- Jak to działa? — 3 step process -->
    <section class="py-16 md:py-24 bg-slate-50 border-b border-slate-100 overflow-hidden" data-aos="fade-up">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">
        
        <div class="text-center mb-16">
          <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-50 text-brand-800 text-xs font-bold mb-4 border border-brand-100 shadow-sm">
            <span class="w-2 h-2 rounded-full bg-brand-600 animate-pulse"></span>
            PROSTY PROCES
          </div>
          <h2 class="text-3xl md:text-4xl font-black text-slate-900 tracking-tight mb-4">Jak to działa?</h2>
          <p class="text-slate-600 text-lg max-w-2xl mx-auto">Cały proces od kontaktu do płatności trwa zaledwie kilka godzin. Zero biurokracji, zero czekania.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 lg:gap-12 relative">
          
          <!-- Connecting line (desktop only) -->
          <div class="hidden md:block absolute top-16 left-[20%] right-[20%] h-0.5 bg-gradient-to-r from-brand-200 via-brand-400 to-brand-200 z-0"></div>

          <!-- Step 1 -->
          <div class="relative z-10 text-center group" data-aos="fade-up" data-aos-delay="0">
            <div class="w-32 h-32 mx-auto mb-6 bg-white rounded-2xl shadow-lg border border-slate-100 flex items-center justify-center group-hover:shadow-xl group-hover:border-brand-200 transition-all duration-300 group-hover:-translate-y-1">
              <div class="relative">
                <PhoneCall class="w-12 h-12 text-brand-600" />
                <span class="absolute -top-2 -right-3 w-7 h-7 bg-brand-600 text-white text-sm font-black rounded-full flex items-center justify-center shadow-md">1</span>
              </div>
            </div>
            <h3 class="text-xl font-bold text-slate-900 mb-2">Zadzwoń do nas</h3>
            <p class="text-slate-600 text-sm leading-relaxed max-w-xs mx-auto">Zadzwoń i podaj ile sztuk bydła chcesz sprzedać. Ustalamy termin odbioru — nawet na ten sam dzień.</p>
          </div>

          <!-- Step 2 -->
          <div class="relative z-10 text-center group" data-aos="fade-up" data-aos-delay="150">
            <div class="w-32 h-32 mx-auto mb-6 bg-white rounded-2xl shadow-lg border border-slate-100 flex items-center justify-center group-hover:shadow-xl group-hover:border-brand-200 transition-all duration-300 group-hover:-translate-y-1">
              <div class="relative">
                <Truck class="w-12 h-12 text-brand-600" />
                <span class="absolute -top-2 -right-3 w-7 h-7 bg-brand-600 text-white text-sm font-black rounded-full flex items-center justify-center shadow-md">2</span>
              </div>
            </div>
            <h3 class="text-xl font-bold text-slate-900 mb-2">Przyjeżdżamy i ważymy</h3>
            <p class="text-slate-600 text-sm leading-relaxed max-w-xs mx-auto">Nasz transport przyjeżdża na miejsce. Ważymy bydło na legalizowanej wadze elektronicznej w Twojej obecności.</p>
          </div>

          <!-- Step 3 -->
          <div class="relative z-10 text-center group" data-aos="fade-up" data-aos-delay="300">
            <div class="w-32 h-32 mx-auto mb-6 bg-white rounded-2xl shadow-lg border border-slate-100 flex items-center justify-center group-hover:shadow-xl group-hover:border-brand-200 transition-all duration-300 group-hover:-translate-y-1">
              <div class="relative">
                <Handshake class="w-12 h-12 text-brand-600" />
                <span class="absolute -top-2 -right-3 w-7 h-7 bg-brand-600 text-white text-sm font-black rounded-full flex items-center justify-center shadow-md">3</span>
              </div>
            </div>
            <h3 class="text-xl font-bold text-slate-900 mb-2">Płacimy gotówką</h3>
            <p class="text-slate-600 text-sm leading-relaxed max-w-xs mx-auto">Natychmiast po ustaleniu ceny płacimy gotówką do ręki lub przelewem. Szybko, uczciwie i bez komplikacji.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- O firmie — dark CTA section -->
    <section class="relative py-20 md:py-28 bg-brand-950 overflow-hidden" data-aos="fade-up">
      <!-- Background pattern -->
      <div class="absolute inset-0 opacity-5 bg-[url('https://www.transparenttextures.com/patterns/cubes.png')]"></div>
      <!-- Decorative gradient -->
      <div class="absolute inset-0 bg-gradient-to-br from-brand-900/50 via-transparent to-brand-950"></div>
      
      <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 items-center">
          
          <!-- Text content -->
          <div data-aos="fade-right">
            <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-800/50 text-brand-300 text-xs font-bold mb-6 border border-brand-700/30">
              <ShieldCheck class="w-3.5 h-3.5" />
              ZAUFAJ DOŚWIADCZENIU
            </div>
            <h2 class="text-3xl md:text-4xl font-black text-white tracking-tight mb-6 leading-tight">
              Firma z <span class="text-brand-400">tradycją</span> i<br>szacunkiem do rolnika.
            </h2>
            <p class="text-brand-100/80 text-base md:text-lg leading-relaxed mb-6">
              Nazywam się <strong class="text-white">Marcin Kiedel</strong> i od ponad 18 lat prowadzę firmę Logos. Przez ten czas zbudowałem relacje z setkami rolników z całego województwa zachodniopomorskiego.
            </p>
            <p class="text-brand-100/80 text-base md:text-lg leading-relaxed mb-8">
              Szanuję ciężką pracę rolnika — dlatego stawiam na <strong class="text-white">uczciwość, terminowość</strong> i <strong class="text-white">rzetelne warunki</strong>. Każda transakcja to moje słowo honoru.
            </p>
            <RouterLink to="/o-nas" class="inline-flex items-center gap-2 px-6 py-3 text-sm font-bold rounded-xl text-brand-950 bg-brand-400 hover:bg-brand-300 transition-all shadow-lg hover:shadow-brand-400/20 active:scale-95 group">
              Poznaj naszą historię
              <ArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
            </RouterLink>
          </div>

          <!-- Image / visual -->
          <div class="relative" data-aos="fade-left" data-aos-delay="200">
            <div class="relative rounded-2xl overflow-hidden shadow-2xl border border-brand-800/30">
              <img src="/wmremove-transformed.webp" alt="Transport bydła - firma Logos" class="w-full h-80 lg:h-96 object-cover" loading="lazy" decoding="async" width="800" height="384" />
              <div class="absolute inset-0 bg-gradient-to-t from-brand-950/60 via-transparent to-transparent"></div>
              <!-- Floating badge -->
              <div class="absolute bottom-4 left-4 right-4 flex justify-between items-end">
                <div class="bg-white/95 backdrop-blur-md px-4 py-2.5 rounded-lg shadow-lg">
                  <p class="text-xs text-slate-500 font-bold uppercase tracking-wider">Doświadczenie</p>
                  <p class="text-xl font-black text-slate-900">18+ lat</p>
                </div>
                <div class="bg-white/95 backdrop-blur-md px-4 py-2.5 rounded-lg shadow-lg">
                  <p class="text-xs text-slate-500 font-bold uppercase tracking-wider">Region</p>
                  <p class="text-xl font-black text-slate-900">Cała Polska</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Liczby mówią same — stats section -->
    <section class="py-16 md:py-20 bg-white border-b border-slate-100" data-aos="fade-up">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">
        
        <div class="text-center mb-14">
          <h2 class="text-3xl md:text-4xl font-black text-slate-900 tracking-tight mb-4">Liczby mówią same</h2>
          <p class="text-slate-600 text-lg max-w-2xl mx-auto">Nasze wyniki to efekt lat ciężkiej pracy i zaufania rolników z całego regionu.</p>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-4 gap-6 md:gap-8">
          
          <!-- Stat 1 -->
          <div class="relative bg-slate-50 rounded-2xl p-6 md:p-8 text-center border border-slate-100 hover:border-brand-200 hover:shadow-lg transition-all duration-300 group" data-aos="fade-up" data-aos-delay="0">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-50 rounded-xl flex items-center justify-center text-brand-600 group-hover:scale-110 transition-transform">
              <Clock class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-slate-900 mb-1">18+</p>
            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Lat na rynku</p>
          </div>

          <!-- Stat 2 -->
          <div class="relative bg-slate-50 rounded-2xl p-6 md:p-8 text-center border border-slate-100 hover:border-brand-200 hover:shadow-lg transition-all duration-300 group" data-aos="fade-up" data-aos-delay="100">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-50 rounded-xl flex items-center justify-center text-brand-600 group-hover:scale-110 transition-transform">
              <Users class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-slate-900 mb-1">1000+</p>
            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Rolników</p>
          </div>

          <!-- Stat 3 -->
          <div class="relative bg-slate-50 rounded-2xl p-6 md:p-8 text-center border border-slate-100 hover:border-brand-200 hover:shadow-lg transition-all duration-300 group" data-aos="fade-up" data-aos-delay="200">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-50 rounded-xl flex items-center justify-center text-brand-600 group-hover:scale-110 transition-transform">
              <Timer class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-slate-900 mb-1">24h</p>
            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Czas reakcji</p>
          </div>

          <!-- Stat 4 -->
          <div class="relative bg-slate-50 rounded-2xl p-6 md:p-8 text-center border border-slate-100 hover:border-brand-200 hover:shadow-lg transition-all duration-300 group" data-aos="fade-up" data-aos-delay="300">
            <div class="w-12 h-12 mx-auto mb-4 bg-brand-50 rounded-xl flex items-center justify-center text-brand-600 group-hover:scale-110 transition-transform">
              <MapPin class="w-6 h-6" />
            </div>
            <p class="text-3xl md:text-4xl font-black text-slate-900 mb-1">Cała</p>
            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Polska</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Zadzwoń teraz — final CTA section -->
    <section class="relative py-16 md:py-20 bg-gradient-to-br from-brand-50 via-white to-brand-50 overflow-hidden" data-aos="fade-up">
      <!-- Decorative circles -->
      <div class="absolute top-0 right-0 w-72 h-72 bg-brand-100/30 rounded-full -translate-y-1/2 translate-x-1/3 blur-3xl pointer-events-none"></div>
      <div class="absolute bottom-0 left-0 w-96 h-96 bg-brand-100/20 rounded-full translate-y-1/2 -translate-x-1/3 blur-3xl pointer-events-none"></div>
      
      <div class="max-w-4xl mx-auto px-6 lg:px-8 relative z-10 text-center">
        <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-100 text-brand-800 text-xs font-bold mb-6 border border-brand-200 shadow-sm" data-aos="fade-up">
          <Phone class="w-3.5 h-3.5" />
          SKONTAKTUJ SIĘ Z NAMI
        </div>
        
        <h2 class="text-3xl md:text-5xl font-black text-slate-900 tracking-tight mb-6 leading-tight" data-aos="fade-up" data-aos-delay="100">
          Umów się na odbiór<br>
          <span class="text-brand-600">jeszcze dziś.</span>
        </h2>
        
        <p class="text-slate-600 text-lg max-w-xl mx-auto mb-10 leading-relaxed" data-aos="fade-up" data-aos-delay="200">
          Jeden telefon wystarczy. Podpowiemy Ci najlepsze warunki sprzedaży i umówimy się na wygodny termin odbioru.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center" data-aos="fade-up" data-aos-delay="300">
          <a href="tel:+48533255214" class="inline-flex items-center justify-center gap-3 px-8 py-4 text-lg font-bold rounded-2xl text-white bg-brand-700 hover:bg-brand-800 transition-all shadow-xl hover:shadow-brand-700/30 active:scale-95 group">
            <Phone class="w-5 h-5 group-hover:animate-pulse" />
            +48 533 255 214
          </a>
          <span class="text-slate-400 text-sm font-medium hidden sm:block">lub</span>
          <RouterLink to="/kontakt" class="inline-flex items-center justify-center gap-2 px-8 py-4 border border-slate-200 text-base font-bold rounded-2xl text-slate-700 bg-white hover:bg-slate-50 transition-all shadow-sm hover:border-brand-200 active:bg-slate-100">
            Napisz do nas
            <ArrowRight class="w-4 h-4" />
          </RouterLink>
        </div>

        <!-- Trust micro-badges -->
        <div class="flex flex-wrap justify-center gap-6 mt-10 text-sm text-slate-500" data-aos="fade-up" data-aos-delay="400">
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
