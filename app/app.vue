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
        <CronicaContent :hermanos="hermanos" />

        <!-- Sello final -->
      <div class="flex items-center justify-center my-10">
        <img class="w-52 seal-stamp" src="/logoSanAntonPig.png" alt="San Antón">
      </div>
      </div>
    </div>
</template>
