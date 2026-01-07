<script setup lang="ts">
import hermanos from '~/data/hermanos2025.json'

// SEO y Meta tags para compartir en redes sociales
const siteUrl = 'https://san-anton.vercel.app'

useSeoMeta({
  title: 'CRÓNICA SAN ANTÓN 2025',
  description: 'La Cofradía de San Antón de Jadraque celebra su edición número 86, alcanzando ya la cifra de 108 hermanos (101 adultos y 7 infantiles)...',
  ogTitle: 'CRÓNICA SAN ANTÓN 2025',
  ogDescription: 'La Cofradía de San Antón de Jadraque celebra su edición número 86, alcanzando ya la cifra de 108 hermanos (101 adultos y 7 infantiles)...',
  ogImage: `${siteUrl}/cofradia-og.jpg`,
  ogImageWidth: '1200',
  ogImageHeight: '630',
  ogImageType: 'image/jpeg',
  ogImageAlt: 'Cofradía de San Antonio Abad - Jadraque',
  ogUrl: siteUrl,
  ogType: 'article',
  ogSiteName: 'Cofradía de San Antón',
  twitterCard: 'summary_large_image',
  twitterTitle: 'CRÓNICA SAN ANTÓN 2025',
  twitterDescription: 'La Cofradía de San Antón de Jadraque celebra su edición número 86, alcanzando ya la cifra de 108 hermanos (101 adultos y 7 infantiles)...',
  twitterImage: `${siteUrl}/cofradia-og.jpg`,
  twitterImageAlt: 'Cofradía de San Antonio Abad - Jadraque',
})

useHead({
  htmlAttrs: {
    lang: 'es'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/logoSanAntonPig.png'
    }
  ]
})

// Scroll reveal animation
onMounted(() => {
  const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -100px 0px'
  }

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('revealed')
        observer.unobserve(entry.target)
      }
    })
  }, observerOptions)

  // Observar todos los elementos con clase scroll-reveal y seal-stamp
  document.querySelectorAll('.scroll-reveal, .seal-stamp').forEach(el => {
    observer.observe(el)
  })
})
</script>
<template>
    <div class="min-h-screen bg-gradient-to-b from-[#fff0d6] to-white">
      <!-- Contenedor principal centrado -->
      <div class="max-w-5xl mx-auto px-3 py-6 md:px-8 md:py-12">
        <header class="flex items-center justify-center mb-10 animate-fade-in">
          <img class="w-full max-w-3xl mx-auto" src="/cofradia.png" alt="San Antón">
        </header>
        <section class="max-w-3xl mx-auto space-y-6 p-5 md:px-8 md:py-10 bg-white/30 backdrop-blur-sm rounded-lg shadow-xl">
        <!-- Título principal -->
        <h2 class="text-4xl font-bold text-secondary-700 gottic text-center mb-2 animate-fade-in-up delay-200">
          CRÓNICA SAN ANTÓN 2025
        </h2>
        <p class="text-center text-secondary-600 italic text-2xl mb-8 mt-5 animate-fade-in-up delay-300">
          Año del 150 aniversario del nacimiento del poeta Antonio Machado
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700 drop-cap animate-fade-in-up delay-400">
          La Cofradía de San Antón de Jadraque celebra su edición número 86, alcanzando ya la cifra de
          108 hermanos (101 adultos y 7 infantiles). Un más que considerable número de cofrades
          que obliga a cambiar el sistema de pago. Por primera vez, y para desahogar espacio en la sacristía
          el día del Santo, se permite pagar la cuota por adelantado en la tienda de la familia Llamas.
        </p>

        <!-- Vísperas -->
        <h2 class="text-3xl font-bold text-primary-700 gottic mt-12 mb-4 border-b-2 border-primary-200 pb-2 scroll-reveal">
          Vísperas · Día 16 de enero
        </h2>

        <p class="mt-4 text-xl leading-relaxed text-gray-700 scroll-reveal">
          A las cinco y media de la tarde, con rigurosa puntualidad, aparece en la Plaza de las Posadas
          nuestra querida charanga Alegría Alcarreña. Poco a poco fueron llegando los hermanos,
          mientras los cohetes sobrevolaban el cielo del pueblo.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          La comitiva se dirigió a la casa del mayordomo saliente, Alberto Serrano Gamo, siendo recibido por
          su padre, Luis, antiguo mayordomo. Tras los refrigerios, se marchó a la iglesia para la misa de vísperas.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          La celebración fue novedosa y participativa. Alberto López "Tarrita" y Álvaro Torres Marina realizaron
          las lecturas, mientras el Padre Juan amenizaba la ceremonia con su guitarra. Se produjo el tradicional
          intercambio del bastón y la toma de posesión del nuevo mayordomo, Rubén Castillejo.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          Tras la misa, la celebración continuó en casa del mayordomo y posteriormente en la ronda de bares:
          Cafetería Grena, La Corona de Jadraque y el hostal, con música, manteos y un ambiente cada vez más animado.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          La noche continuó con las luminarias de Casas Nuevas, San Roque y el Peaje, entre rosquillas,
          licores, música y una multitudinaria participación que dejó imágenes memorables.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          La charanga siguió tocando hasta altas horas de la madrugada y la fiesta terminó en la peña
          El Chispazo, prolongándose hasta bien entrada la mañana.
        </p>

        <!-- San Antón -->
        <h2 class="text-3xl font-bold text-primary-700 gottic mt-12 mb-4 border-b-2 border-primary-200 pb-2 scroll-reveal">
          San Antón · Día 17 de enero
        </h2>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          Los hermanos fueron apareciendo para disfrutar del día del Santo, acompañados por los gaiteros
          de Sigüenza. Tras la misa y la procesión, se celebró la bendición de animales y la fotografía grupal.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          Después del habitual recorrido de bares, se celebró la comida en el restaurante Cuatro Caminos.
        </p>

        <h3 class="text-2xl font-bold text-secondary-600 gottic mt-8 mb-3 scroll-reveal">Menú</h3>
        <ul class="mt-4 space-y-2 list-disc list-inside text-xl text-gray-700 ml-4">
          <li>Entrantes: pimientos rellenos, langostinos cocidos y setas</li>
          <li>Segundo: bacalao o lomo de ternera</li>
          <li>Postre y café</li>
        </ul>

        <p class="mt-6 text-xl leading-relaxed text-gray-700">
          Uno de los momentos más esperados fue el pesaje de los nuevos hermanos.
        </p>

        <h3 class="text-2xl font-bold text-secondary-600 gottic mt-8 mb-4 scroll-reveal">Pesaje de los nuevos hermanos</h3>
        <div class="overflow-x-auto mt-4 scroll-reveal">
          <table class="w-full border-collapse bg-white shadow-lg rounded-lg overflow-hidden">
            <thead>
              <tr class="bg-primary-700 text-white">
                <th class="px-4 py-3 text-left text-sm font-semibold uppercase tracking-wider">Nombre</th>
                <th class="px-4 py-3 text-center text-sm font-semibold uppercase tracking-wider">Peso (kg)</th>
                <th class="px-4 py-3 text-center text-sm font-semibold uppercase tracking-wider">Arrobas</th>
              </tr>
            </thead>
            <tbody class="divide-y divide-gray-200">
              <tr
                v-for="(hermano, index) in hermanos"
                :key="index"
                :class="[
                  'hover:bg-primary-50 transition-colors',
                  index % 2 !== 0 ? 'bg-gray-50' : ''
                ]"
              >
                <td class="px-4 py-4 text-gray-800">{{ hermano.nombre }}</td>
                <td class="px-4 py-4 text-center text-gray-800">{{ hermano.peso }}</td>
                <td class="px-4 py-4 text-center text-gray-800">{{ hermano.arrobas }}</td>
              </tr>
            </tbody>
          </table>
        </div>

        <p class="mt-6 text-xl leading-relaxed text-gray-700">
          La comida estuvo amenizada por una banda de mariachis, que cantó rancheras de mesa en mesa,
          convirtiéndose en una de las grandes novedades de esta edición.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          Ya por la noche, los más jóvenes organizaron un baile popular en el Bar La Corona, prolongando
          la celebración hasta bien entrada la madrugada.
        </p>

        <!-- Sorteo y sobras -->
        <h2 class="text-3xl font-bold text-primary-700 gottic mt-12 mb-4 border-b-2 border-primary-200 pb-2 scroll-reveal">
          Sorteo y sobras · Día 18 de enero
        </h2>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          A las 11:30 dio comienzo el tradicional sorteo del cerdo. Tras casi una hora, salió el número
          1.780, resultando ganador Javier Criado.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          La última ronda de bares recorrió Casino, Grena, Alto Rey, Hostal El Castillo y Cuatro Caminos,
          finalizando con las tradicionales judías en el Justi.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          La sobremesa estuvo llena de anécdotas, mus, baile y buen humor, prolongándose durante toda la tarde.
        </p>

        <!-- Epílogo -->
        <h2 class="text-3xl font-bold text-primary-700 gottic mt-12 mb-4 border-b-2 border-primary-200 pb-2 scroll-reveal">
          Epílogo
        </h2>

        <p class="mt-4 text-xl leading-relaxed text-gray-700">
          Esta crónica no estaría completa sin mencionar el emotivo detalle de Isabel Calvo, quien regaló
          el sombrero de su padre Pedro Calvo para que siguiera presente en San Antón.
        </p>

        <p class="mt-4 text-xl leading-relaxed text-gray-700 mb-12">
          Así terminó un San Antón 2025 inolvidable, reflejo del gran momento que vive la cofradía y de
          una familia que no deja de crecer. Nos espera un 2026 apasionante. ¡A por él!
        </p>
      </section>

      <!-- Sello final -->
      <div class="flex items-center justify-center my-10">
        <img class="w-52 seal-stamp" src="/logoSanAntonPig.png" alt="San Antón">
      </div>
      </div>
    </div>
</template>
